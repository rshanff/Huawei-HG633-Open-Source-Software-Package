#
# Makefile for the IEEE 802.1d ethernet bridging layer.
#

obj-$(CONFIG_BRIDGE) += bridge.o

bridge-y	:= br.o br_device.o br_fdb.o br_forward.o br_if.o br_input.o \
			br_ioctl.o br_notify.o br_stp.o br_stp_bpdu.o \
			br_stp_if.o br_stp_timer.o br_netlink.o
bridge-$(CONFIG_MIPS_BRCM) += br_flows.o

bridge-$(CONFIG_SYSFS) += br_sysfs_if.o br_sysfs_br.o


bridge-$(CONFIG_IGMP_SNOOPING) += br_igmp_snooping.o

bridge-$(CONFIG_BR_IGMP_SNOOP) += br_mcast.o

bridge-$(CONFIG_BR_IGMP_SNOOP) += br_netlink_mcpd.o

bridge-$(CONFIG_BR_IGMP_SNOOP) += br_igmp_parse.o

bridge-$(CONFIG_BR_IGMP_SNOOP) += br_igmp_dev_list.o

bridge-$(CONFIG_MLD_SNOOPING) += br_mld_snooping.o

bridge-$(CONFIG_BR_IGMP_SNOOP) += br_igmp.o

bridge-$(CONFIG_BR_MLD_SNOOP) += br_mld.o

bridge-$(CONFIG_BRIDGE_NETFILTER) += br_netfilter.o

bridge-$(CONFIG_BR_IGMP_STATISTIC) += br_igmp_statistic.o

ifeq ($(strip $(CONFIG_BR_MLD_SNOOP)),y)
bridge-$(CONFIG_BR_MLD_SNOOP) += br_netlink_mcpd.o br_mcast.o
endif

bridge-$(CONFIG_MIPS_BRCM) += br_notifier.o

bridge-$(CONFIG_ATP_BR_VLAN_MODE) += br_vlan.o

obj-$(CONFIG_BRIDGE_NF_EBTABLES) += netfilter/
