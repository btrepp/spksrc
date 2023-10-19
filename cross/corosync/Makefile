PKG_NAME = corosync
PKG_VERS = 3.1.7
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/corosync/corosync/releases/download/v$(PKG_VERS)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = cross/libqb

HOMEPAGE = hhttps://corosync.github.io/corosync/
COMMENT  = The corosync cluster engine 
LICENSE  = BSD 

# gcc >= 5.1 required
REQUIRED_MIN_DSM = 7.0
UNSUPPORTED_ARCHS = comcerto2k


GNU_CONFIGURE = 1

PRE_CONFIGURE_TARGET = corosync_pre_configure

include ../../mk/spksrc.cross-cc.mk

corosync_pre_configure:
	$(RUN) ./autogen.sh
