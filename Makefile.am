ACLOCAL_AMFLAGS=-I m4
lib_LTLIBRARIES = libinterflop_checkcancellation.la

if ENABLE_LTO
LTO_FLAGS = -flto
else
LTO_FLAGS =
endif

if ENABLE_WARNINGS
WARNING_FLAGS = -Wall -Wextra -Wno-varargs
else
WARNING_FLAGS =
endif

libinterflop_checkcancellation_la_SOURCES = \
    interflop_checkcancellation.cxx

libinterflop_checkcancellation_la_CFLAGS = \
    -I@INTERFLOP_INCLUDEDIR@/ \
    -fno-stack-protector \
    $(LTO_FLAGS) -Og \
    $(WARNING_FLAGS)

libinterflop_checkcancellation_la_CXXFLAGS = \
    -I@INTERFLOP_INCLUDEDIR@/ \
    -fno-stack-protector \
    $(LTO_FLAGS) -Og \
    $(WARNING_FLAGS)

libinterflop_checkcancellation_la_LDFLAGS = \
    $(LTO_FLAGS) -Og

libinterflop_checkcancellation_la_LIBADD = \
    @INTERFLOP_LIBDIR@/libinterflop_logger.la \
    @INTERFLOP_LIBDIR@/libinterflop_stdlib.la

includesdir=$(includedir)/interflop
includes_HEADERS= interflop_checkcancellation.h
