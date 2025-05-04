# configure.ac for virt

AC_INIT([virt], [0.1.0], [snambakam@tejasvin.com])
AM_INIT_AUTOMAKE([-Wall -Werror foreign subdir-objects])
#AC_CONFIG_SRCDIR([src/tools/virt/main.c])
AC_CONFIG_HEADERS([src/include/config.h:build/config.h.in])
AC_PREFIX_DEFAULT(/usr)

# Checks for programs.
AC_PROG_CC
AM_PROG_AR
LT_INIT

case "${host_os}:${host_cpu}" in
    linux*:x86_64)
        PLATFORM_LIB_PREFIX=lib64
        ;;
    linux*:aarch64)
        PLATFORM_LIB_PREFIX=lib
        ;;
    *)
        AC_ERROR("Unsupported operating system - ${host_os}:${host_cpu}")
        ;;
esac

CPPFLAGS="$CPPFLAGS -D_REENTRANT -D_GNU_SOURCE -fPIC"

AM_CPPFLAGS="$AM_CPPFLAGS -I${top_srcdir}/include"
AM_CFLAGS="$AM_CFLAGS -Wall -Werror -fno-strict-aliasing"

# Optional: Check for required tools/libraries
# For example, to check for pkg-config:
# PKG_PROG_PKG_CONFIG

# Checks for libraries.
# AC_CHECK_LIB([m], [sin])  # Example: check for libm

# Checks for header files.
AC_CHECK_HEADERS([stdlib.h stdint stdio.h string.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_SIZE_T

# Checks for library functions.
AC_CHECK_FUNCS([memset strdup])

# Generate output files
AC_CONFIG_FILES([
    Makefile
    src/Makefile
    src/common/Makefile
    src/tools/Makefile
    src/tools/virt/Makefile
])
AC_OUTPUT
