SUBDIRS = include src

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = xmu.pc xmuu.pc

EXTRA_DIST = \
	xmu.pc.in \
	xmuu.pc.in \
	include/X11/Xmu/WhitePoint.h \
	ChangeLog

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
