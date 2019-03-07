# 3.5 Contiki 开始了！

开始编译我们的第一个 Contiki 例程！打开终端，执行：

```text
cd examples/hello-world
make TARGET=zoul savetarget
```

这将告诉 Contiki 为 RE-Mote 平台编译 hello-world 例程。如果要使用Z1平台，执行：

```text
make TARGET=z1 savetarget
```

对于每个应用，你只需要做一遍上面的操作。编译应用程序：

```text
make hello-world
```

如果没产生问题，将有类似下面的输出：

```text
CC symbols.c
AR contiki-z1.a
CC hello-world.c
CC ../../platform/z1/./contiki-z1-main.c
LD hello-world.z1
rm obj_z1/contiki-z1-main.o hello-world.co
```

文件夹中应该生成一个文件hello-world.z1。接下来我们烧写程序到设备。

任何时候，你可以在编译时重新定义目标并覆盖原来保存的目标：

```text
make TARGET=zoul hello-world
CC hello-world.c
LD hello-world.elf
arm-none-eabi-objcopy -O binary --gap-fill 0xff hello-world.elf hello-world.bin
```

这将忽略原先保存的文件Makefile.target，直接使用zoul作为目标。

