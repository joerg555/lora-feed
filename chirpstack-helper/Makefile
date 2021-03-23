# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.

include $(TOPDIR)/rules.mk

PKG_NAME:=chirpstack-help
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/chirpstack-helper
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=LoRaWAN
  TITLE:=Helper script to setup chirpstack und pgsql postgres database
  PKGARCH:=all
endef

define Package/chirpstack-appmeta
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=LoRaWAN
  TITLE:=apps chirpstack, pgsql and mosquitto
  PKGARCH:=all
  DEPENDS:=chirpstack-application-server chirpstack-network-server chirpstack-helper mosquitto-ssl pgsql-cli pgsql-server redis
endef

define Build/Prepare
	#mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Compile
	#
endef

define Package/chirpstack-helper/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) ./files/chirpstack-helper $(1)/usr/bin
endef

define Package/chirpstack-appmeta/install
	#
endef

$(eval $(call BuildPackage,chirpstack-appmeta))
$(eval $(call BuildPackage,chirpstack-helper))
