include $(TOPDIR)/rules.mk

PKG_NAME:=input-event-daemon
PKG_BUILD_PARALLEL:=1
PKG_VERSION:=0.1.3
PKG_INSTALL:=1
PKG_RELEASE:=1
PKG_REV:=8b0c8f117e093b89927cf966c008954a11717e10

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_PROTO:=git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=https://github.com/gandro/input-event-daemon.git
PKG_SOURCE_VERSION:=v$(PKG_VERSION)


include $(INCLUDE_DIR)/package.mk

define Package/input-event-daemon
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=input event daemon
  URL:=https://github.com/gandro/input-event-daemon
endef

define Package/input-event-daemon/description
  input-event-daemon -  input event handling daemon for linux
endef

define Build/Configure
endef

define Package/input-event-daemon/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/input-event-daemon $(1)/usr/bin
	$(INSTALL_DIR) $(1)/etc
	$(INSTALL_BIN) ./files/sample.conf $(1)/etc/input-event-daemon.conf
	$(INSTALL_BIN) ./files/sample_touch.conf $(1)/etc/input-event-daemon-touch.conf
endef


$(eval $(call BuildPackage,input-event-daemon))
