| https://makefiletutorial.com/
| https://github.com/Kitware/CMake/blob/master/Help/dev/documentation.rst
|

Adding .PHONY to a target will prevent make from confusing the phony target with a file name. In this example, if the file “clean” is created, **make clean** will still be run. 
Without .PHONY clean, **make clean**: 'clean' is up to date.

| touch clean
| .PHONY clean
| clean: 
      do something
      
      
 - wildcards: *, ?, [...]
 - %: which matches any zero or more characters
 - $@: automatic variable that contains the target name.
 - "$(VARIALBE_NAME)"
 - @echo vs echo
 - 
.. code-block:: 
    
    # Minimal makefile for Sphinx documentation

    # You can set these variables from the command line.
    SPHINXOPTS    =
    SPHINXBUILD   = sphinx-build
    SPHINXPROJ    = Testproject
    SOURCEDIR     = .
    BUILDDIR      = _build

    # Set default "make" without argument, "make == make help"
    help:
    	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

    .PHONY: help Makefile

    # Catch-all target: route all unknown targets to Sphinx using the new
    # "make mode" option.  
    # $(O) is meant as a shortcut for $(SPHINXOPTS).
    %: Makefile
    	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
 
