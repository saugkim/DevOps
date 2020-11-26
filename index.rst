.. Test project documentation master file, created by sphinx-quickstart 

DevOps Aalto
==============

.. toctree::
   :maxdepth: 2
   :hidden:
   
   Content/about_course.rst
   Content/learning_devops.rst
   Content/about_yaml.rst
   Content/GUI_for_ubuntu.rst
   Content/understand_makefile.rst


About Project CS-EJ4104-Fall Aalto
************************************

The project builds a simple site by using the Hugo static website generator and a continuous deployment pipeline with GitHub Actions.

Task description The goal of the project is to create your personal website. Instead of using the built-in website generator in GitHub Pages, we will use a third-party tool: Hugo, a framework for building static websites that takes Markdown documents as input and produces HTML files as output. We will configure a continuous delivery pipeline through GitHub Actions to trigger a build and (if that is successful) publish the site on GitHub Pages.

For the project, you must use the GitHub repository we created for you under the cs-ej4104-fall-2020 organization on GitHub. The name of the repository is the same as your GitHub account. The repository is private and the course staff has access to it. Refer to the tutorial on& version control with git on how to get started. You should receive a notification email about the repository once it is successfully created. Just make sure to check the email address associated with your GitHub account.

We are going to use two branches for this project: the master branch for the source (Markdown) files used by Hugo, and the gh-pages branch to publish the site. First of all, you have to create the gh-pages branch on the remote repository. After that, you have to enable GitHub pages under the corresponding section under the repository settings (i.e., through the Settings tab on the far right, under the repository name). Make sure to pick the gh-pages branch option from the pull-down menu under Source. Once configured, you should be able to see the following message: Your site is ready to be published at, followed by the corresponding address. You most likely have to wait for some time before the message turns into Your site is published at and actually see the content of the site. Note that the content of this branch will be created through the continuous deployment pipeline, so the actual files therein do not matter at this stage as long as the branch exists and is configured as the source of GitHub Pages. See also the official documentation for a more detailed description.

After this preliminary configuration, you can start making the website for real. First of all, you can go through this interactive tutorial on how to quickly write Markdown content. Then, you may want to install Hugo on your computer for testing purposes. You can follow the installation instructions here and this tutorial on how to get started with Hugo, just skip the part after Configure Hugo for deployment on the latter. Once you have created the source of the website, just push it on the master branch of the project repository. 

Again, remember that the content in the website is public. Links to the blog posts described next. You are free to add other content (for instance, to practice with Hugo) as long as you have the three items above.
