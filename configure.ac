AC_PREREQ(2.52)

AC_INIT([Apertium English-Sajem Tan], [0.2.0], [popcorn.tomato.dude@gmail.com], [apertium-eng-sjt], [http://wiki.apertium.org/wiki/Apertium-eng-sjt])
AM_INIT_AUTOMAKE

AC_PROG_LN_S
AC_PROG_AWK

m4_define([required_apertium_version], [3.4.0])
PKG_CHECK_MODULES(APERTIUM, apertium >= required_apertium_version, [], [PKG_CHECK_MODULES(APERTIUM, apertium-3.2 >= required_apertium_version)])



AC_PATH_PROG([RTXCOMP], [rtx-comp], [false], [$PATH$PATH_SEPARATOR$with_rtx_comp/bin])
AS_IF([test x$RTXCOMP = xfalse], [AC_MSG_ERROR([You don't have rtx-comp installed])])

AC_PATH_PROG([RTXPROC], [rtx-proc], [false], [$PATH$PATH_SEPARATOR$with_rtx_proc/bin])
AS_IF([test x$RTXPROC = xfalse], [AC_MSG_ERROR([You don't have rtx-proc installed])])

AC_PATH_PROGS(ZCAT, [gzcat zcat], [false])
AS_IF([test x$ZCAT = xfalse], [AC_MSG_ERROR([You don't have zcat nor gzcat installed])])

AP_MKINCLUDE

AC_OUTPUT([Makefile])

