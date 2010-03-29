SUBDIRS = include src

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = xmu.pc xmuu.pc

MAINTAINERCLEANFILES = ChangeLog INSTALL
EXTRA_DIST = include/X11/Xmu/WhitePoint.h

.PHONY: ChangeLog INSTALL

INSTALL:
	$(INSTALL_CMD)

ChangeLog:
	$(CHANGELOG_CMD)

dist-hook: ChangeLog INSTALL

if LINT
# Check source code with tools like lint & sparse
lint:
	(cd src && $(MAKE) $(MFLAGS) lint)
endif LINT
