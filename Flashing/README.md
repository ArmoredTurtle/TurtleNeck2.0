TN2 Flashing Steps
--------------------------------
cd ~/klipper
make menuconfig

[*] Enable extra low-level configuration options
    Micro-controller Architecture (STMicroelectronics STM32) --->
    Processor model (STM32G0B1) --->
    Bootloader offset (No bootloader) --->
    Clock Reference (8 MHz crystal) --->
    Communication interface (USB (on PA11/PA12)) --->
    USB ids --->
()  GPIO pins to set at micro-controller startup

#
<img width="490" alt="TN_Firmware" src="https://github.com/user-attachments/assets/060938bf-8d48-4d00-af47-611a78ab9f4a">
#
When config is complete type 'q' to exit then select 'Yes' to save the config
type make clean followed by make to build the klipper firmware


Verify the TN2 is in DFU mode with lsusb. If you dont see a DFU device hold the boot button and press reset then run the lsusb command again

Run make flash FLASH_DEVICE=Device ID

The prompt File downloaded successfully indicates the writing was completed. There will be error messages following this that say dfu-util:Error during download get_status. This is normal just ignore it.

After the firmware write is completed run

ls /dev/serial/by-id/

to get the device serial ID

Plug this ID into the turtleneckv2.cfg in the serial section




To update firmware
cd ~/klipper
make menuconfig

[*] Enable extra low-level configuration options
    Micro-controller Architecture (STMicroelectronics STM32) --->
    Processor model (STM32G0B1) --->
    Bootloader offset (No bootloader) --->
    Clock Reference (8 MHz crystal) --->
    Communication interface (USB (on PA11/PA12)) --->
    USB ids --->
()  GPIO pins to set at micro-controller startup

When config is complete type 'q' to exit then select 'Yes' to save the config
type make clean followed by make to build the klipper firmware

To flash

make flash FLASH_DEVICE=/dev/serial/by-id/**Your device serialID**

The prompt File downloaded successfully indicates the writing was completed. There will be error messages following this that say dfu-util:Error during download get_status. This is normal just ignore it.
