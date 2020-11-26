| https://makefiletutorial.com/
| https://github.com/Kitware/CMake/blob/master/Help/dev/documentation.rst
|

.. code-block:: Makefile
    :linenos:
   
    # Minimal makefile for Sphinx documentation

    # You can set these variables from the command line.
    SPHINXOPTS    =
    SPHINXBUILD   = sphinx-build
    SPHINXPROJ    = Testproject
    SOURCEDIR     = .
    BUILDDIR      = _build

    # Put it first so that "make" without argument is like "make help".
    help:
    	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

    .PHONY: help Makefile

    # Catch-all target: route all unknown targets to Sphinx using the new
    # "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
    %: Makefilw
    	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
 
