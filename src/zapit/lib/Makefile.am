AM_CPPFLAGS = -fno-rtti -fno-exceptions

AM_CPPFLAGS += \
	@HWLIB_CFLAGS@ \
	-I$(top_builddir) \
	-I$(top_srcdir) \
	-I$(top_srcdir)/src \
	-I$(top_srcdir)/src/zapit/include \
	-I$(top_srcdir)/lib \
	-I$(top_srcdir)/lib/libeventserver \
	-I$(top_srcdir)/lib/libconfigfile

noinst_LIBRARIES = libzapitclient.a
libzapitclient_a_SOURCES = zapitclient.cpp zapittools.cpp
