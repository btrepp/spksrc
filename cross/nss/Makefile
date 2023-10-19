PKG_NAME = nss
PKG_VERS = 3.88
PKG_VERS_UNDER= $(shell echo -n $(PKG_VERS) | tr . _)
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://ftp.mozilla.org/pub/mozilla.org/security/nss/releases/NSS_$(PKG_VERS_UNDER)_RTM/src
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)/nss

DEPENDS = cross/nspr

HOMEPAGE = https://firefox-source-docs.mozilla.org/security/nss/index.html 
COMMENT  = a set of libraries designed to support cross-platform development of security-enabled client and server applications
LICENSE  = GPLv2

# gcc >= 5.1 required
REQUIRED_MIN_DSM = 7.0
UNSUPPORTED_ARCHS = comcerto2k

GNU_CONFIGURE = 0 

CONFIGURE_TARGET = nop
COMPILE_MAKE_OPTIONS = USE_64=1 all 
ADDITIONAL_CFLAGS=-I $(STAGING_INSTALL_PREFIX)/include/nspr
ADDITIONAL_LDFLAGS= -L$(STAGING_INSTALL_PREFIX)/lib

$PRE_CONFIGURE_TARGET = kronosnet_pre_configure

include ../../mk/spksrc.cross-cc.mk

#kronosnet_pre_configure:
#	$(RUN) ./autogen.sh
