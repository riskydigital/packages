#
# Copyright (C) 2017-2018 Daniel Engberg <daniel.engberg.lists@pyret.net>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=tio
PKG_VERSION:=1.29
PKG_RELEASE:=1
PKG_MAINTAINER:=
PKG_LICENSE:=GPL-2.0+
PKG_LICENSE_FILES:=COPYING

PKG_SOURCE_URL:=https://github.com/$(PKG_NAME)/$(PKG_NAME)/releases/download/v$(PKG_VERSION)/
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_HASH:=371a11b69dd2e1b1af3ca2a1c570408b1452ae4523fe954d250f04b6b2147d23

PKG_FIXUP:=autoreconf

include $(INCLUDE_DIR)/package.mk

define Package/tio
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A simple TTY terminal I/O application
  URL:=https://tio.github.io/
  SUBMENU:=Terminal
endef

define Package/tio/description
  A small and simple TTY terminal I/O application
endef

define Package/tio/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/tio $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,tio))
