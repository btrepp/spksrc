PKG_NAME = kronosnet
PKG_VERS = 1.28
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://kronosnet.org/releases
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = 

HOMEPAGE = https://kronosnet.org/releases 
COMMENT  = network abstraction layer designed for High Availability use cases 
LICENSE  = LGPL2.1

# gcc >= 5.1 required
REQUIRED_MIN_DSM = 7.0
UNSUPPORTED_ARCHS = comcerto2k

GNU_CONFIGURE = 1

PRE_CONFIGURE_TARGET = kronosnet_pre_configure

include ../../mk/spksrc.cross-cc.mk

kronosnet_pre_configure:
	$(RUN) ./autogen.sh
