My attempt at making an easy to build an initramFS Linux image for RISC-V testing.

**Prerequistes**
* A compatible riscv linux toolchain.

**Default Flow**

This builds an image using the default linux and busybox configurations (`./linux_config`, `./busybox_config`). It auto-generates and initramfs.txt and uses a dummy profile script.
You can specify a diretory whose content you want to pack in linux by setting the DIRNAME when making linux. Its content will be placed under a directory called celio in your linux. (Please do not have a / at the end of the path?)

    $ git submodule update --init
    $ make DIRNAME=/a/cool/directory/you/want/to/pack/in/linux

**Augmenting the image**

Set `./profile` to get what you need on bootup. Look at Makefile for how to change things.

Of course, you can always change the linux and busybox configurations.
