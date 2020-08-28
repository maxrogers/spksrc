PKG_NAME = Radarr
PKG_VERS = 3.0.0.3502
PKG_EXT = tar.gz
PKG_DIST_NAME = Radarr.aphrodite.$(PKG_VERS).linux.tar.gz
PKG_DIST_SITE = https://www.dropbox.com/s/zxki8mrtgn7dwte
PKG_DIR = Radarr

DEPENDS =

HOMEPAGE = https://radarr.video/
COMMENT  = Radarr is a movie manager like Couchpotato, but based on the Sonarr codebase. It can monitor multiple RSS feeds for new movie releases and will grab, sorts and rename them. It can also be configured to automatically upgrade the quality of files already downloaded if a better quality format becomes available.
LICENSE  = GNU GPL v3

CONFIGURE_TARGET = nop
COMPILE_TARGET = nop
INSTALL_TARGET = myInstall

include ../../mk/spksrc.cross-cc.mk

myInstall:
	mkdir -p $(STAGING_INSTALL_PREFIX)/share/$(PKG_DIR)
	tar -cf - -C $(WORK_DIR)/$(PKG_DIR) . | tar -xf - -C $(STAGING_INSTALL_PREFIX)/share/$(PKG_DIR)
