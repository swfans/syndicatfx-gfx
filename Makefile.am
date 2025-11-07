ACLOCAL_AMFLAGS = --install -I m4


docs_DATA = README.md gfx_config.h
docsdir = $(prefix)/$(PARENT_PACKAGE)

EXTRA_DIST = 

install-data-hook:
	cd "$(DESTDIR)${prefix}/$(PARENT_PACKAGE)"; \
	mv README.md gfx_readme.md
