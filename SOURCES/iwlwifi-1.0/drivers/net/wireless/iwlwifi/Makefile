# common
CONFIG_WIRELESS=y
CONFIG_CFG80211=y
CONFIG_CFG80211_DEFAULT_PS=y
CONFIG_CFG80211_CRDA_SUPPORT=y
CONFIG_MAC80211=m
CONFIG_MAC80211_HAS_RC=y
CONFIG_MAC80211_RC_MINSTREL=y
CONFIG_MAC80211_RC_MINSTREL_HT=y
CONFIG_MAC80211_RC_DEFAULT_MINSTREL=y
CONFIG_MAC80211_RC_DEFAULT="minstrel_ht"
CONFIG_MAC80211_LEDS=y
CONFIG_MAC80211_STA_HASH_MAX_SIZE=0
CONFIG_WLAN=y
CONFIG_IWLWIFI=m
CONFIG_IWLWIFI_LEDS=y
CONFIG_IWLDVM=m
CONFIG_IWLWIFI_OPMODE_MODULAR=y

CONFIG_IWLWIFI_DEVICE_TRACING=n
CONFIG_RTL_CARDS=m

obj-$(CONFIG_IWLWIFI)	+= iwlwifi.o
iwlwifi-objs		+= iwl-io.o
iwlwifi-objs		+= iwl-drv.o
iwlwifi-objs		+= iwl-debug.o
iwlwifi-objs		+= iwl-notif-wait.o
iwlwifi-objs		+= iwl-eeprom-read.o iwl-eeprom-parse.o
iwlwifi-objs		+= iwl-phy-db.o iwl-nvm-parse.o
iwlwifi-objs		+= pcie/drv.o pcie/rx.o pcie/tx.o pcie/trans.o
iwlwifi-$(CONFIG_IWLDVM) += iwl-1000.o iwl-2000.o iwl-5000.o iwl-6000.o
iwlwifi-$(CONFIG_IWLMVM) += iwl-7000.o iwl-8000.o
iwlwifi-objs		+= iwl-trans.o

iwlwifi-objs += $(iwlwifi-m)

iwlwifi-$(CONFIG_IWLWIFI_DEVICE_TRACING) += iwl-devtrace.o

ccflags-y += -D__CHECK_ENDIAN__ -I$(src)

obj-$(CONFIG_IWLDVM)	+= dvm/
obj-$(CONFIG_IWLMVM)	+= mvm/

CFLAGS_iwl-devtrace.o := -I$(src)
