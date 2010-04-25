AC_INIT([fingerd], [0.0+], [rjk@greenend.org.uk])
AC_CONFIG_AUX_DIR([config.aux])
AM_INIT_AUTOMAKE([fingerd], [0.0])
AC_CONFIG_SRCDIR([fingerd.c])
AM_CONFIG_HEADER([config.h])
AC_PROG_CC
if test "x$GCC" = xyes; then
  CC="${CC} -Wall -W -Wpointer-arith -Wbad-function-cast -Wwrite-strings -Wmissing-prototypes -Wmissing-declarations -Wnested-externs -Wshadow"
  CC="${CC} -Werror"
  CC="${CC} -std=gnu99"
fi
AC_CONFIG_FILES([Makefile])
AC_OUTPUT
