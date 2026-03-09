# MagneticSwitch & POT Module
This module is a convenient prototyping board for building user interfaces for audio devices such as MIDI controllers, synthesizers, and mixers. It features 10 magnetic switches, 12 potentiometers (POTs), and 10 RGB LEDs.

## how to buy
Yamamoto Works Ltd. Online Store

## specifications
- VCC: 3.3-5V
- Analog Mux: [TI CD74HC4067M96](https://www.ti.com/product/ja-jp/CD74HC4067/part-details/CD74HC4067M96)
- POT: [Alps RK09K1130A5R(10k)](https://tech.alpsalpine.com/e/products/detail/RK09K1130A5R/) x12
- Hall Effect Sensor: [TI DRV5056A8QDBZR](https://www.ti.com/product/ja-jp/DRV5056/part-details/DRV5056A3QDBZR) x10
- RGB LED: [Würth Elektronik WL-ICLED 1312020030000](https://www.we-online.com/en/components/products/WL-ICLED?sq=1312020030000#1312020030000) x10

## supported magnetic switches
- [Gateron Low Profile Magnetic Jade Pro HE](https://www.gateron.com/products/gateron-full-pom-low-profile-magnetic-jade-pro-switch-set?VariantsId=10870)
- [Gateron Low Profile Magnetic Jade HE](https://www.gateron.com/products/gateron-low-profile-magnetic-jade-switch?VariantsId=10872)

## features
- Six magnetic switches (KEY0–5) can be connected directly to the microcontroller board’s analog input pins.
- The twelve POTs (RV1–12) and four magnetic switches (SUB_KEY6–9) are routed through a CD74HC4067M96 analog multiplexer. By driving S0–S3, you can read 16 channels of analog values from AIN.
- The RGB LEDs (1312020030000) are addressable and use a NeoPixel-compatible (WS2812-style) single-wire control interface.

## size
<img width="1265" height="872" alt="image" src="https://github.com/user-attachments/assets/98adf1cb-027a-4b6b-b143-2f5456ff5548" />

## photo

## License
The hardware design files in this repository are licensed under the
**CERN Open Hardware Licence Version 2 - Permissive (CERN-OHL-P-2.0)**.

Unless otherwise stated, the following are treated as hardware design files covered by CERN-OHL-P-2.0:

- KiCad schematic files
- PCB layout files

A copy of the license text is provided in the `LICENSE` file.
