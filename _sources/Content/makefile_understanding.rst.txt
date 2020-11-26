$(VARIABLE_NAME)
*****************
| VARIABLE = sphinx-build 
| use like this $(VARIABLE)
| call variable, Makefile variable is only string

@echo 
******
what is this @? silence

.. code-block::

      target: # with @
            @echo "Call gcc to generate $@"
      --> Call gcc to generate target
      
      target:  # without @ 
            echo "Call gcc to generate $@"
      --> echo "Call gcc to generate target"
      --> Call gcc to generate target


.PHONY 
*******
Adding .PHONY to a target will prevent make from confusing the phony target with a file name. In this example, if the file “clean” is created, **make clean** will still be run. 

| Without *.PHONY clean*, $ make clean: 'clean' is up to date  #there is 'clean' file
| With *.PHONY clean*, $ make-clean: do clean

.. code-block::

      touch clean
      .PHONY clean
      clean: 
            do clean


$@: $<
**********
automatic variable *$@* matches the target name, *$<* matches the prerequisite name

.. code-block::

      target: prerequisite
            @echo "Call gcc to generate $@ from $<"
      prerequisite:
            @echo "Do something"
      # Do something
      # Call gcc to generate target from prerequisite
      

$(0) 
*****
in sphinx, $(0) is shortcut for $(SPHINXOPTS).

sphinx build command
*********************
| *sphinx-build -b buildername source_directory build_directory [filenames...]*
| default builder is html
| -M: alternative to -b. Uses the Sphinx make_mode module. default html

.. code-block::
      
      %: Makefile
    	      @$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
      html: Makefile
            @$(SPHINXBUILD) -M html "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)


- wildcards: *, ?, [...]
- %: which matches any zero or more characters


Makefile sample (which is used for this DevOps project)
********************************************************
.. code-block:: 
    
    # Minimal makefile for Sphinx documentation
    # You can set these VARIABLES from the command line.
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


| https://makefiletutorial.com/
