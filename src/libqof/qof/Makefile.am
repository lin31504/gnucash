include $(top_srcdir)/test-templates/Makefile.decl
SUBDIRS = . test
TEST_SUBDIRS = test

lib_LTLIBRARIES = libgnc-qof.la

libgnc_qof_la_LDFLAGS= \
	-version-info \
	$(LIBQOF_LIBRARY_VERSION)

libgnc_qof_common_libs =  \
  $(GLIB_LIBS) \
  $(REGEX_LIBS) \
  $(top_builddir)/lib/libc/libc-missing.la

libgnc_qof_la_LIBADD = $(libgnc_qof_common_libs)

AM_CPPFLAGS = \
  -I$(top_srcdir)/lib/libc \
  -I$(top_srcdir)/src \
  $(GLIB_CFLAGS) \
  $(BOOST_CPPFLAGS)

libgnc_qof_la_SOURCES =  \
   gnc-aqbanking-templates.cpp \
   gnc-date.cpp        \
   gnc-int128.cpp      \
   gnc-numeric.cpp     \
   gnc-rational.cpp    \
   gnc-timezone.cpp    \
   gnc-datetime.cpp    \
   guid.cpp            \
   kvp_frame.cpp       \
   kvp-value.cpp       \
   qof-backend.cpp      \
   qofbook.cpp         \
   qofchoice.cpp       \
   qofclass.cpp        \
   qofevent.cpp        \
   qofid.cpp           \
   qofinstance.cpp     \
   qoflog.cpp          \
   qofobject.cpp       \
   qofquery.cpp        \
   qofquerycore.cpp    \
   qofsession.cpp      \
   qof-string-cache.cpp  \
   qofutil.cpp

qofincludedir = ${pkgincludedir}

qofinclude_HEADERS = \
   gnc-aqbanking-templates.h \
   gnc-date-p.h      \
   gnc-date.h        \
   gnc-numeric.h     \
   gnc-rational.hpp  \
   gnc-timezone.hpp  \
   gnc-datetime.hpp  \
   guid.h            \
   kvp_frame.hpp     \
   kvp-value.hpp     \
   qof.h             \
   qof-backend.hpp   \
   qofbackend.h      \
   qofbook.h         \
   qofbookslots.h    \
   qofchoice.h       \
   qofclass.h        \
   qofevent.h        \
   qofid-p.h         \
   qofid.h           \
   qofinstance-p.h   \
   qofinstance.h     \
   qoflog.h          \
   qofobject.h       \
   qofquery.h        \
   qofquerycore.h    \
   qofsession.h      \
   qofsession.hpp    \
   qof-string-cache.h  \
   qofutil.h         \
   qof-gobject.h

noinst_HEADERS = \
   gnc-backend-prov.hpp \
   qofbook-p.h  \
   qofclass-p.h  \
   qofevent-p.h \
   gnc-int128.hpp  \
   qofobject-p.h  \
   qofquery-p.h  \
   qofquerycore-p.h

if OS_WIN32
libgnc_qof_la_SOURCES += qof-win32.cpp
else
EXTRA_DIST += qof-win32.cpp
endif

AM_CPPFLAGS += -DG_LOG_DOMAIN=\"qof\"
