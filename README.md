# MagneticSwitch & POT Module
This module is a convenient prototyping board for building user interfaces for audio devices such as MIDI controllers, synthesizers, and mixers. It features 10 magnetic switches, 12 potentiometers (POTs), and 10 RGB LEDs.

## How to buy
- [Tindie(International)](https://www.tindie.com/products/yamamotoworks/magneticsw-and-pot-module/)  
- [BASE(Japan)](https://miyworks.base.shop/items/139586742)

## Specifications
- VCC: 3.3-5V
- Analog Mux: [Onsemi MC74HC4067A](https://www.onsemi.com/products/timing-logic-memory/standard-logic/multiplexers/mc74hc4067a)
- POT: [Alps RK09K1130A5R(10k)](https://tech.alpsalpine.com/e/products/detail/RK09K1130A5R/) x12
- Hall Effect Sensor: [TI DRV5056A8QDBZR](https://www.ti.com/product/ja-jp/DRV5056/part-details/DRV5056A3QDBZR) x10
- RGB LED: [Würth Elektronik WL-ICLED 1312020030000](https://www.we-online.com/en/components/products/WL-ICLED?sq=1312020030000#1312020030000) x10

## Supported magnetic switches
- [Gateron Low Profile Magnetic Jade Pro HE](https://www.gateron.com/products/gateron-full-pom-low-profile-magnetic-jade-pro-switch-set?VariantsId=10870)
- [Gateron Low Profile Magnetic Jade HE](https://www.gateron.com/products/gateron-low-profile-magnetic-jade-switch?VariantsId=10872)

## Features
- Six magnetic switches (KEY0–5) can be connected directly to your microcontroller’s ADC pins.
- The twelve POTs (RV1–12) and four magnetic switches (SUB_KEY6–9) are routed through an **MC74HC4067ADWR2G** analog multiplexer. By driving **S0–S3**, you can select one of 16 channels and read its analog value from **AIN**.
  - The channel mapping is shown below:
  
    | S0 | S1 | S2 | S3 | AIN source |
    |----|----|----|----|------------|
    | L  | L  | L  | L  | RV1        |
    | H  | L  | L  | L  | RV2        |
    | L  | H  | L  | L  | RV3        |
    | H  | H  | L  | L  | RV4        |
    | L  | L  | H  | L  | RV5        |
    | H  | L  | H  | L  | RV6        |
    | L  | H  | H  | L  | RV7        |
    | H  | H  | H  | L  | RV8        |
    | L  | L  | L  | H  | RV9        |
    | H  | L  | L  | H  | RV10       |
    | L  | H  | L  | H  | RV11       |
    | H  | H  | L  | H  | RV12       |
    | L  | L  | H  | H  | SUB_KEY6   |
    | H  | L  | H  | H  | SUB_KEY7   |
    | L  | H  | H  | H  | SUB_KEY8   |
    | H  | H  | H  | H  | SUB_KEY9   |

- The RGB LEDs (1312020030000) are addressable and use a NeoPixel-compatible (WS2812-style) single-wire control interface.

## Application Example
- [JUMBLEQ](https://github.com/yamamo2shun1/JUMBLEQ)

## Size
<img width="1265" height="872" alt="image" src="https://github.com/user-attachments/assets/98adf1cb-027a-4b6b-b143-2f5456ff5548" />

## Photo
![DSCF7952](https://github.com/user-attachments/assets/5b7fc943-0b36-4156-b9b5-7d7c80b38f15)
![DSCF7964](https://github.com/user-attachments/assets/0779d37d-fd60-4b52-a8a6-09363335ce6b)

## License
The hardware design files in this repository are licensed under the
**CERN Open Hardware Licence Version 2 - Permissive (CERN-OHL-P-2.0)**.

Unless otherwise stated, the following are treated as hardware design files covered by CERN-OHL-P-2.0:

- KiCad schematic files
- PCB layout files

A copy of the license text is provided in the `LICENSE` file.
