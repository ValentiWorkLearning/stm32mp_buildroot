## Build default image
```shell
make BR2_EXTERNAL=${REPO_ROOT} -C buildroot O=${REPO_ROOT}/image_build/ stm32mp157c_dk2_defconfig
make 2>&1 | tee build.log
```
