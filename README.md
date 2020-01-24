**This example is deprecated. The [mbed-os-example-cpu-stats](https://os.mbed.com/teams/mbed-os-examples/code/mbed-os-example-cpu-stats/) example shows how to use the `mbed_stats_cpu_get` API to print the CPU usage.**

# Getting started with CPU Usage on Mbed OS

This guide reviews the steps required to get CPU usage on Mbed OS platform.

Please install [mbed CLI](https://github.com/ARMmbed/mbed-cli#installing-mbed-cli).

## Import the example application

From the command-line, import the example:

```
mbed import mbed-os-example-cpu-usage
cd mbed-os-example-cpu-usage
```

### Now compile

Invoke `mbed compile`, and specify the name of your platform and your favorite toolchain (`GCC_ARM`, `ARM`, `IAR`). For example, for the ARM Compiler 5:

```
mbed compile -m K64F -t ARM
```

Your PC may take a few minutes to compile your code. At the end, you see the following result:

```
[snip]
+------------------+-------+-------+------+
| Module           | .text | .data | .bss |
+------------------+-------+-------+------+
| [lib]\c_w.l      | 11473 |    16 |  348 |
| [lib]\cpprt_w.l  |    36 |     0 |    0 |
| [lib]\fz_wm.l    |    18 |     0 |    0 |
| [lib]\m_wm.l     |    48 |     0 |    0 |
| anon$$obj.o      |    32 |     0 | 1024 |
| main.o           |   490 |    16 |    0 |
| mbed-os\drivers  |   165 |     0 |    0 |
| mbed-os\events   |  2139 |     8 | 1568 |
| mbed-os\features |   132 |     0 |  304 |
| mbed-os\hal      |  1910 |    34 |  128 |
| mbed-os\platform |  3695 |   104 |  604 |
| mbed-os\rtos     | 17302 |  2310 | 4592 |
| mbed-os\targets  | 10707 |   112 |  324 |
| Subtotals        | 48147 |  2600 | 8892 |
+------------------+-------+-------+------+
Total Static RAM memory (data + bss): 11492 bytes
Total Flash memory (text + data): 50747 bytes

Image: .\BUILD\K64F\ARM\mbed-os-example-cpu-usage.bin

```

### Program your board

1. Connect your Mbed device to the computer over USB.
1. Copy the binary file to the Mbed device.
1. Press the reset button to start the program.

### License and contributions
The software is provided under Apache-2.0 license. Contributions to this project are accepted under the same license. Please see contributing.md for more info.

This project contains code from other projects. The original license text is included in those source files. They must comply with our license guide
