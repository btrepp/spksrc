PKG_NAME = nspr
PKG_VERS = 4.35
PKG_VERS_UNDER= $(shell echo -n $(PKG_VERS) | tr . _)
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://ftp.mozilla.org/pub/nspr/releases/v$(PKG_VERS)/src
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)/nspr

# DEPENDS = cross/glibc-latest 

HOMEPAGE = https://firefox-source-docs.mozilla.org/nspr/index.html 
COMMENT  = a platform-neutral API for system level and libc-like functions 
LICENSE  = GPLv2

# gcc >= 5.1 required
REQUIRED_MIN_DSM = 7.0
UNSUPPORTED_ARCHS = comcerto2k

GNU_CONFIGURE = 1 
CONFIGURE_ARGS = --enable-64bit

$PRE_CONFIGURE_TARGET = kronosnet_pre_configure

include ../../mk/spksrc.cross-cc.mk

#kronosnet_pre_configure:
#	$(RUN) ./autogen.sh
