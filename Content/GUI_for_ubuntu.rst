Set up GUI in Ubuntu LTS
===========================

How to set up GUI in Ubuntu LTS
*********************************

I have a project(c++ programming) in Linux system(I am bit familiar with Linux system, but current device is windows, I need to run ubuntu in my machine. And I need also graphic user interface for the project(I tried to use Aalto lyta or vdi, but users have no permission to install any library). This is for setup graphic user interface in Ubuntu LTS(ubuntu lts already installed).

Current version: Ubuntu 20.04 

Installing WSL with GUI using VcXsrv
***************************************
Windows Subsystem for Linux is a feature in Windows 10 where you can install and run Linux applications on Windows 10. Though keep in mind ... Dhanar Santika blog https://medium.com/@dhanar.santika/installing-wsl-with-gui-using-vcxsrv-6f307e96fac0

Download VcXsrv  
*******************
| VcXsrv is a Windows X-server based on the xorg git sources.  
| https://sourceforge.net/projects/vcxsrv/

XLaunch and setup
*********************
 - choose window option, One Large Window or Fullscreen option?
 - choose Start no client. 
 - check Disable access control.  
| blank screen will appear. close or keep open.

install Desktop Environment for WSL 
**************************************
 - XFCE4, KDE, GNOME, LXDE, Cinnamon, MATE, etc.

| In ubuntu WSL
.. code-block:: bash

  $ sudo apt-get install xfce4
  $ echo 'export DISPLAY=:0.0' >> ~/.bashrc 


| Exit and re-run ubuntu and start!
.. code-block:: bash

  $ startxfce4


| In Bash, open Windows File Explorer:
.. code-block:: bash

  explorer.exe .

