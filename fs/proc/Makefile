# SPDX-License-Identifier: GPL-2.0
#
# Makefile for the Linux proc filesystem routines.
#

obj-y   += proc.o

CFLAGS_task_mmu.o	+= $(call cc-option,-Wno-override-init,)
proc-y			:= nommu.o task_nommu.o
proc-$(CONFIG_MMU)	:= task_mmu.o

proc-y       += inode.o root.o base.o generic.o array.o \
		fd.o
proc-$(CONFIG_TTY)      += proc_tty.o
proc-y	+= cmdline.o
proc-y	+= consoles.o
proc-y	+= cpuinfo.o
proc-y	+= devices.o
proc-y	+= interrupts.o
proc-y	+= loadavg.o
proc-y	+= meminfo.o
proc-y	+= stat.o
proc-y	+= uptime.o
proc-y	+= util.o
proc-y	+= version.o
proc-y	+= softirqs.o
proc-y	+= namespaces.o
proc-y	+= self.o
proc-y	+= thread_self.o
proc-$(CONFIG_PROC_UID)  += uid.o
proc-$(CONFIG_PROC_SYSCTL)	+= proc_sysctl.o
proc-$(CONFIG_NET)		+= proc_net.o
proc-$(CONFIG_PROC_KCORE)	+= kcore.o
proc-$(CONFIG_PROC_VMCORE)	+= vmcore.o
proc-$(CONFIG_PRINTK)	+= kmsg.o
proc-$(CONFIG_PROC_PAGE_MONITOR)	+= page.o
#ifdef VENDOR_EDIT
#Huacai.Zhou@PSW.BSP.kernel.Peformance, 2018/06/18, add foreground process opt support
obj-y	+= oppo_healthinfo/
#endif /* VENDOR_EDIT */
#ifdef VENDOR_EDIT
#Hailong.Liu@TECH.Kernel.CPU, 2019/10/24, stat cpu usage on each tick.
proc-y	+= task_cpustats.o
#endif /* VENDOR_EDIT */
