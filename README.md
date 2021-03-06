# macOS cross compiler for Raspberry Pi (rpi)

Very simple setup for cross compiler on macOS for Raspberry Pi. 

## Steps to setup and test cross compiler on macOS

- **case sensitive volume needed for crosstool-ng**
  - _this script helps you create a new case sensitive volume for compiling code_
  -  remote bash - `bash <(wget -qO- https://raw.githubusercontent.com/Artistan/mac-os-cross-compile-arm-rpi-linux-gnueabihf/master/case-sensitive-volume.sh)`
  -  local git clone - `./case-sensitive-volume.sh`
- **setup the crosstool-ng build environment for raspberry pi.**
  - _this script sets up all the needed packages to properly compile a cross compiler instance on macOS_
  -  cd into the case sensitive volume, optionally go into a sub-directory...
  -  remote bash - `bash <(wget -qO- https://raw.githubusercontent.com/Artistan/mac-os-cross-compile-arm-rpi-linux-gnueabihf/master/crosstool-ng-setup.sh)`
  -  local git clone - `./crosstool-ng-setup.sh`
- **ct-ng build**
  - _this script simply starts a ct-ng build process with your current configuration_
  -  same directory
  -  remote bash - `bash <(wget -qO- https://raw.githubusercontent.com/Artistan/mac-os-cross-compile-arm-rpi-linux-gnueabihf/master/ct-ng-build.sh)`
  -  local git clone - `./ct-ng-build.sh`
- **test compile example**
  - _this script will use the built arm-rpi3-linux-gnueabihf-gcc to compile test, upload to pi, and execute the file_
  -  same directory
  -  remote bash - `bash <(wget -qO- https://raw.githubusercontent.com/Artistan/mac-os-cross-compile-arm-rpi-linux-gnueabihf/master/rpi-test.sh)`
  -  local git clone - `./rpi-test.sh`

## other resources

- **example configs**
    -  https://medium.com/coinmonks/setup-gcc-8-1-cross-compiler-toolchain-for-raspberry-pi-3-on-macos-high-sierra-cb3fc8b6443e
    -  https://github.com/crosstool-ng/crosstool-ng/blob/master/samples/armv8-rpi3-linux-gnueabihf/crosstool.config
    -  https://www.jaredwolff.com/toolchains/#hide1
- **older compiles**
    - https://www.bootc.net/archives/2012/05/26/how-to-build-a-cross-compiler-for-your-raspberry-pi/
- **arm tools**
    -  https://developer.arm.com/open-source/gnu-toolchain/gnu-rm
    