# bcm4329
DHDCFLAGS = -DBCMDRIVER -DBCMDONGLEHOST -DDHDTHREAD -DBCMWPA2 \
	-DUNRELEASEDCHIP -DDHD_GPL -DDHD_SCHED -DBDC -DTOE -DDHD_BCMEVENTS \
	-DSHOW_EVENTS -DSDIO_ISR_THREAD -DBCMSDIO -DDHD_GPL -DBCMLXSDMMC \
	-DBCMPLATFORM_BUS -DLINUX -DSOFTAP -DDHD_DEBUG -DCONFIG_WIRELESS_EXT \
	-DARP_OFFLOAD_SUPPORT -DPKT_FILTER_SUPPORT -DMMC_SDIO_FORCE_PULLUP    \
	-DMMC_SDIO_BROKEN_CCCR_REV -DEMBEDDED_PLATFORM \
	-DCUSTOMER_HW4 -DCUSTOM_RESET_GPIO_NUM=97 \
	-Wall -Wstrict-prototypes -Werror  \
	-Idrivers/net/wireless/bcm4329 -Idrivers/net/wireless/bcm4329/include

DHDOFILES = dhd_linux.o linux_osl.o bcmutils.o dhd_common.o dhd_custom_gpio.o \
	wl_iw.o siutils.o sbutils.o aiutils.o hndpmu.o bcmwifi.o dhd_sdio.o   \
	dhd_linux_sched.o dhd_cdc.o bcmsdh_sdmmc.o bcmsdh.o bcmsdh_linux.o    \
	bcmsdh_sdmmc_linux.o

obj-$(CONFIG_BCM4329) += dhd.o
dhd-objs += $(DHDOFILES)
EXTRA_CFLAGS = $(DHDCFLAGS)
EXTRA_LDFLAGS += --strip-debug
