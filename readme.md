# Rust boilerplate for stm32f103c8t6

## Hardware

* [Blue Pill](https://www.aliexpress.com/wholesale?SearchText=stm32f103c8t6)
* [ST-LINK V2](https://www.aliexpress.com/wholesale?SearchText=stlink+v2)

## Setup

`direnv allow`

## Udev rules

```
services.udev.extraRules = ''
  # STMicroelectronics ST-LINK/V2
  ATTR{idVendor}=="0483", ATTR{idProduct}=="3748", MODE="660", GROUP="dialout"
'';
```

## Build

`cargo build --release`

## Flash

`cargo flash --chip stm32f103C8 --release`

```
    Finished release [optimized] target(s) in 0.02s
    Flashing /home/ksevelyar/code/arm-sandbox/target/thumbv7m-none-eabi/release/blue-pill-boilerplate
     Erasing sectors ✔ [00:00:00] [##################################]  1.00KiB/ 1.00KiB @ 18.64KiB/s (eta 0s )
 Programming pages   ✔ [00:00:00] [##################################]  1.00KiB/ 1.00KiB @ 10.83KiB/s (eta 0s )
    Finished in 0.134s
```
