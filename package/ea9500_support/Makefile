#
# Copyright (C) 2019 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ea9500_support
PKG_VERSION:=1
PKG_RELEASE:=1

PKG_MAINTAINER:=Kenneth Kasilag <kenneth@kasilag.me>

SCAN_DEPS = *.mk

include $(INCLUDE_DIR)/package.mk

define Package/ea9500_support
  SECTION:=base
  CATEGORY:=Base system
  TITLE:=$(1)
endef

define Package/base-files/description
 This package contains scripts to support the Linksys EA9500 (linksys,panamera).
endef

define Build/Compile

endef

define Package/ea9500_support/install
	# Make dual boot behave
	$(INSTALL_DIR) $(1)/etc/init.d/
	$(INSTALL_BIN) ./files/etc/init.d/clear_partialboot $(1)/etc/init.d/clear_partialboot
endef

$(eval $(call BuildPackage,ea9500_support))
