# Minimal makefile for Sphinx documentation
# https://www.sphinx-doc.org/en/master/man/sphinx-build.html

# You can set these variables from the command line, and also
# from the environment for the first two.
SPHINXOPTS    ?= --verbose --show-traceback --keep-going --color --nitpicky --jobs auto
SPHINXBUILD   ?= sphinx-build
SOURCEDIR     = source
BUILDDIR      = .build
FORCE_COLOR   = true

# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

livehtml:
	sphinx-autobuild -a "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O) -b=dirhtml --open-browser --delay 0
