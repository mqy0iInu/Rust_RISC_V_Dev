# RISC-V MCU Develop
Rust Personal Development Repository for the RISC-V MCU.

# Target
| MCU           | Rsut Env | Price | Flash | SRAM | Clock  | GPIO | ADC        | UART | I2C | SPI |
| ------------- | ---------| ------|-------|------|--------|------|------------|------|-----|-----|
| CH32V003F4P6  | no-std   | ￠20  | 16KB  | 2KB  | 48MHz  | 18   | 10bit  8ch | 1ch  | 1ch | 1ch |
| CH32V203C8T6  | no-std   | ＄ 1  | 64KB  | 20KB | 144MHz | 37   | 12bit 20ch | 4ch  | 2ch | 2ch |
| ESP32-C3      | std      | ＄ 3  |  4MB  | 400KB| 160MHz | 22   | 12bit  6ch | 2ch  | 1ch | 2ch |

# Environment
Rust Environment ... `std` and `no std`

## no-std
Example

```rust
#![no_std]
#![no_main]

use riscv_rt::entry;
use panic_halt as _;
use riscv as _;

use ch32v2::ch32v20x as pac;

#[entry]
fn main() -> ! {
     // Code
}
```

# Develop
Please, you must do it.

```shell
rustup target add riscv32imac-unknown-none-elf
```
## Build

```shell
cargo build --release
```