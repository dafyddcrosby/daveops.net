---
title: Building Kernels
tags: ["Fedora"]
---

```bash
dnf install fedpkg fedora-packager rpmdevtools ncurses-devel pesign bison kernel-devel glibc-static
```

TODO - add bison flex to <https://fedoraproject.org/wiki/Building_a_custom_kernel>

### Building a user-mode linux kernel

```
# TODO add a saner config
mini.config
CONFIG_BINFMT_ELF=y
CONFIG_HOSTFS=y
CONFIG_LBD=y
CONFIG_BLK_DEV=y
CONFIG_BLK_DEV_LOOP=y
CONFIG_STDERR_CONSOLE=y
CONFIG_UNIX98_PTYS=y
CONFIG_EXT2_FS=y
```

```bash
# build the config
make ARCH=um allnoconfig KCONFIG_ALLCONFIG=mini.config
# make the kernel
make ARCH=um
```

if missing gnu/stubs-32.h, means you need glibc-devel.i686

