AM_CFLAGS = -I $(top_srcdir)/include

if ENABLE_OVSDB
AM_CFLAGS += -I $(LOCAL_SYSROOT_DIR)/usr/local/include/ovs -DOPS
endif

noinst_LTLIBRARIES = libcommon-daemon-lib.la libcommon-daemon-client.la
include_HEADERS    = lldp-const.h

libcommon_daemon_lib_la_SOURCES = \
	log.c log.h \
	marshal.c marshal.h \
	ctl.c ctl.h \
	lldpd-structs.c lldpd-structs.h lldp-const.h
libcommon_daemon_lib_la_LIBADD  = compat/libcompat.la

libcommon_daemon_client_la_SOURCES = log.c log.h lldp-const.h
libcommon_daemon_client_la_LIBADD  = compat/libcompat.la
