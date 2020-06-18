AM_LIBADD = \
	$(PULSEAUDIO_LIBS) \
	$(DBUS_LIBS) \
	$(DROIDUTIL_LIBS)
AM_CFLAGS = \
	$(PASSTHROUGH_COMMON_CFLAGS) \
	$(PULSEAUDIO_CFLAGS) \
	$(DBUS_CFLAGS) \
	$(DROIDHEADERS_CFLAGS) \
	$(DROIDUTIL_CFLAGS) \
	-DPULSEAUDIO_VERSION=@PA_MAJOR@ \
	-I$(top_srcdir)/src/hidl


modlibexec_LTLIBRARIES = module-droid-hidl$(DROID_MODULE_SUFFIX).la

noinst_HEADERS = module-symdef-compat.h

module_droid_hidl__DROID_MODULE_SUFFIX__la_SOURCES = module-droid-hidl.c
module_droid_hidl__DROID_MODULE_SUFFIX__la_LDFLAGS = -module -avoid-version -Wl,-no-undefined -Wl,-z,noexecstack
module_droid_hidl__DROID_MODULE_SUFFIX__la_LIBADD = $(AM_LIBADD) -lm
module_droid_hidl__DROID_MODULE_SUFFIX__la_CFLAGS = $(AM_CFLAGS) -DPA_MODULE_NAME=module_droid_hidl
