#
# (C) Copyright 2012 Henrik Nordstrom <henrik@henriknordstrom.net>
#
# Based on some other Makefile
# (C) Copyright 2000-2003
# Wolfgang Denk, DENX Software Engineering, wd@denx.de.
#
# SPDX-License-Identifier:	GPL-2.0+
#
obj-y	+= timer.o

obj-$(CONFIG_MACH_SUN6I)	+= tzpc.o
obj-$(CONFIG_MACH_SUN8I_H3)	+= tzpc.o

ifndef CONFIG_SPL_BUILD
ifdef CONFIG_ARMV7_PSCI
obj-$(CONFIG_MACH_SUN6I)	+= psci.o
obj-$(CONFIG_MACH_SUN7I)	+= psci.o
obj-$(CONFIG_MACH_SUN8I)	+= psci.o

obj-$(CONFIG_MACH_SUN5I)	+= psci_suspend.o
obj-$(CONFIG_MACH_SUN7I)	+= psci_suspend.o
endif
endif

ifdef CONFIG_SPL_BUILD
obj-y	+= fel_utils.o
endif
