![](./resources/official_armmbed_example_badge.png)
# CPU Usage Mbed OS Example

The example project is part of the [Arm Mbed OS Official Examples](https://os.mbed.com/code/). It reviews the steps required to get Central Processing Unit (CPU) usage on the Mbed OS platform. It contains an application that can be run on all supported [Mbed boards](https://os.mbed.com/platforms/).

You can build the project with all supported [Mbed OS build tools](https://os.mbed.com/docs/mbed-os/latest/tools/index.html). However, this example project specifically refers to the command line interface tool [Arm Mbed CLI](https://github.com/ARMmbed/mbed-cli#installing-mbed-cli).
(Note: To see a rendered example you can import into the Arm Online Compiler, please see our [import quick start](https://os.mbed.com/docs/mbed-os/latest/quick-start/online-with-the-online-compiler.html#importing-the-code).)

1. [Install Mbed CLI](https://os.mbed.com/docs/mbed-os/latest/quick-start/offline-with-mbed-cli.html).

1. Clone this repository on your system, and change the current directory to where the project was cloned:

    ```bash
    $ git clone git@github.com:armmbed/mbed-os-example-cpu-usage && cd mbed-os-example-cpu-usage
    ```

    Alternatively, you can download the example project with Arm Mbed CLI using the `import` subcommand:

    ```bash
    $ mbed import mbed-os-example-cpu-usage && cd mbed-os-example-cpu-usage
    ```

## Application functionality

The `main()` function creates an event queue and adds a function to periodically print idle and usage information about the CPU. It also starts a thread that blinks an LED at varying intervals in order to keep the CPU busy.

## Building and Running

1. Connect a USB cable between the USB port on the target and the host computer.
2. Run the following command to build the example project and program the microcontroller flash memory:
    ```bash
    $ mbed compile -m <TARGET> -t <TOOLCHAIN> --flash --sterm
    ```

The binary is located at `./BUILD/<TARGET>/<TOOLCHAIN>/mbed-os-example-cpu-usage.bin`.

Alternatively, you can manually copy the binary to the board, which you mount on the host computer over USB.

Depending on the target, you can build the example project with the `GCC_ARM`, `ARM` or `IAR` toolchain. After installing Arm Mbed CLI, run the command below to determine which toolchain supports your target:

```bash
$ mbed compile -S
```

### License and contributions
The software is provided under Apache-2.0 license. Contributions to this project are accepted under the same license. Please see contributing.md for more info.

This project contains code from other projects. The original license text is included in those source files. They must comply with our license guide
