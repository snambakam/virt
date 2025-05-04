# configure.ac for virt

AC_INIT([virt], [0.1.0], [snambakam@tejasvin.com])
AC_CONFIG_SRCDIR([src/tools/virt/main.c])
AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CC

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