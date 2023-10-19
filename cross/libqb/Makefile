PKG_NAME = libqb
PKG_VERS = 2.0.8
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/ClusterLabs/libqb/releases/download/v$(PKG_VERS)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = cross/libxml2

HOMEPAGE = http://clusterlabs.github.io/libqb/ 
COMMENT  = libqb is a library providing high performance logging, tracing, ipc, and poll. 
LICENSE  = LGPL2.1

GNU_CONFIGURE = 1
CONFIGURE_ARGS += --with-libxml2 XML2_CONFIG=$(STAGING_INSTALL_PREFIX)/bin/xml2-config

# gcc >= 5.1 required
REQUIRED_MIN_DSM = 7.0
UNSUPPORTED_ARCHS = comcerto2k

PRE_CONFIGURE_TARGET = libqb_pre_configure

include ../../mk/spksrc.cross-cc.mk

libqb_pre_configure:
	$(RUN) ./autogen.sh
