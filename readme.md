# Rust boilerplate for stm32f103c8t6

## Hardware

* [Blue Pill](https://www.aliexpress.com/wholesale?SearchText=stm32f103c8t6)
* [ST-LINK V2](https://www.aliexpress.com/wholesale?SearchText=stlink+v2)

## Setup

`direnv allow`

## Debug

`cargo flash --list-probes`

```
The following debug probes were found:
[0]: STLink V2 (VID: 0483, PID: 3748, Serial: 091D16002C135437334D4E00, StLink)
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
