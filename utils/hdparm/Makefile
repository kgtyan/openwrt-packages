#
# Copyright (C) 2006-2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=hdparm
PKG_VERSION:=9.37
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=@SF/$(PKG_NAME)
PKG_MD5SUM:=0bb94ddd1bedd5c02b1ca62f1caaf6de

include $(INCLUDE_DIR)/package.mk

define Package/hdparm
  SECTION:=utils
  CATEGORY:=Utilities
  SUBMENU:=disc
  TITLE:=Hard disk drive configuration utilitity
  URL:=http://sourceforge.net/projects/hdparm/
  MAINTAINER:=Luka Perkov <openwrt@lukaperkov.net>
endef

define Package/hdparm/description
 get/set SATA/IDE device parameters
endef

define Package/hdparm/install
	$(INSTALL_DIR) $(1)/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/$(PKG_NAME) $(1)/sbin
endef

$(eval $(call BuildPackage,hdparm))
