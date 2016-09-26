include $(TOPDIR)/rules.mk

PKG_NAME:=umackereld
PKG_VERSION:=0.0.1
PKG_RELEASE:=1

PKG_GITREV:=f77c6aead2100040ad0ce6f46742a44cce31f7f5
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_GITREV)
PKG_SOURCE:=$(PKG_GITREV).zip
PKG_SOURCE_URL:=https://github.com/hanazuki/umackereld/archive/
PKG_MD5SUM:=788877c7cf210881603f9b1dd0b6f7d5

PKG_BUILD_PARALLEL:=1
PKG_INSTALL:=1
PKG_USE_MIPS16:=0

PKG_LICENSE:=Apache-2.0
PKG_MAINTAINER:=Yoshio HANAWA <for-openwrt@hnw.jp>

PKG_FIXUP:=autoreconf

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_SOURCE_SUBDIR)

include $(INCLUDE_DIR)/package.mk

define Package/umackereld
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A small Mackerel agent written in C for OpenWrt
  URL:=https://github.com/hanazuki/umackereld/
  DEPENDS:=+libcurl +libjson-c +libuci
endef

define Package/umackereld/description
  A small Mackerel agent written in C for OpenWrt
endef

define Package/umackereld/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/umackereld $(1)/usr/bin/
endef

$(eval $(call BuildPackage,umackereld))
