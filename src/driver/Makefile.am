AM_CXXFLAGS = -fno-rtti -fno-exceptions -D__STDC_FORMAT_MACROS

SUBDIRS = pictureviewer audiodec

AM_CPPFLAGS = \
	-I$(top_builddir) \
	-I$(top_srcdir) \
	-I$(top_srcdir)/src \
	-I$(top_srcdir)/src/zapit/include \
	-I$(top_srcdir)/lib \
	-I$(top_srcdir)/lib/libnet \
	-I$(top_srcdir)/lib/libconfigfile \
	-I$(top_srcdir)/lib/connection \
	-I$(top_srcdir)/lib/libeventserver \
	@SIGC_CFLAGS@ \
	@FREETYPE_CFLAGS@ \
	@HWLIB_CFLAGS@

noinst_LIBRARIES = libneutrino_driver.a libneutrino_driver_netfile.a

libneutrino_driver_a_SOURCES = \
	abstime.c \
	audiofile.cpp \
	audiometadata.cpp \
	audioplay.cpp \
	colorgradient.cpp \
	fade.cpp \
	fb_window.cpp \
	fbaccel.cpp \
	file.cpp \
	fontrenderer.cpp \
	framebuffer_ng.cpp \
	genpsi.cpp \
	moviecut.cpp \
	neutrinofonts.cpp \
	radiotext.cpp \
	radiotools.cpp \
	rcinput.cpp \
	record.cpp \
	scanepg.cpp \
	screen_max.cpp \
	screenshot.cpp \
	shutdown_count.cpp \
	streamts.cpp \
	volume.cpp

if ENABLE_GRAPHLCD
libneutrino_driver_a_SOURCES += \
	nglcd.cpp
endif

if ENABLE_SHAIRPLAY
libneutrino_driver_a_SOURCES += \
	shairplay.cpp
endif

if BOXTYPE_DUCKBOX
libneutrino_driver_a_SOURCES += \
	vfd.cpp
endif

if BOXTYPE_COOL
libneutrino_driver_a_SOURCES += \
	vfd.cpp

endif
if BOXTYPE_TRIPLE
libneutrino_driver_a_SOURCES += \
	newclock.cpp \
	lcdd.cpp
endif

if BOXTYPE_SPARK
libneutrino_driver_a_SOURCES += \
	simple_display.cpp
endif
if BOXTYPE_AZBOX
libneutrino_driver_a_SOURCES += \
	simple_display.cpp
endif
if BOXTYPE_GENERIC
libneutrino_driver_a_SOURCES += \
	simple_display.cpp
endif
if USE_STB_HAL
AM_CPPFLAGS += \
	@DIRECTFB_CFLAGS@
endif

libneutrino_driver_netfile_a_SOURCES = netfile.cpp

