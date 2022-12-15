## Build default image
```shell
make BR2_EXTERNAL=${REPO_ROOT} -C buildroot O=${REPO_ROOT}/image_build/ stm32mp157c_dk2_defconfig
make 2>&1 | tee build.log
```

## Image flashing
```shell
sudo dd if=${REPO_ROOT}/image_build/images/sdcard.img of=/dev/sdb bs=4M conv=fdatasync status=progress
```

## STM32 Programmer setup
```shell
https://wiki.stmicroelectronics.cn/stm32mpu/wiki/Getting_started/STM32MP1_boards/STM32MP157x-DK2/Let%27s_start/Populate_the_target_and_boot_the_image
export PATH=/home/valenti/STMicroelectronics/STM32Cube/STM32CubeProgrammer/bin:$PATH
sudo apt-get install libusb-1.0-0

```