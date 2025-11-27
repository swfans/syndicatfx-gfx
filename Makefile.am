ACLOCAL_AMFLAGS = --install -I m4

data/mspr-0.tab: data/mspr-0.dat

data/mspr-0.dat: $(top_srcdir)/filelist-mspr-0.txt $(top_srcdir)/data/feproj-std.pal

data/%.dat:
	$(MKDIR_P) "$(@D)"
	$(PNGTORAW) -b -o "$@" -p "$(word 2,$^)" -f sspr -l 0 "$<"

mspr_0_DATA = data/mspr-0.dat data/mspr-0.tab
mspr_0dir = $(prefix)/$(PARENT_PACKAGE)/data

docs_DATA = README.md gfx_config.h
docsdir = $(prefix)/$(PARENT_PACKAGE)

EXTRA_DIST = docs mspr_0

install-data-hook:
	cd "$(DESTDIR)${prefix}/$(PARENT_PACKAGE)"; \
	mv README.md gfx_readme.md
