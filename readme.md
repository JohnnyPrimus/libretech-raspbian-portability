# Libre Computer Raspbian Portability
## Objective
This script is designed to run on existing Raspbian images and enabled them
them to boot on Libre Computer boards. It uses our extensive upstream u-boot
and Linux work and infrastructure to support Raspbian's legacy ARMv6 binaries
as well as their newer ARMv7 and ARMv8 images.

It is a proof-of-concept and there are no warranties implied or otherwise.
We highly recommend backing up the images if they hold important data in case
something unexpected occurs. While they should still boot on your original
device, this is not fully tested or guaranteed so continue at your own risk.

This script installs/configures/overwrites data this device/MicroSD card.
It is designed to run on Raspberry Pi(R)s and requires internet access to 
download additional necessary components. Once the script finishes, the card
should still remain bootable on the original board.


## Supported Distributions
- [Raspbian 10 Buster Lite armhf](https://www.raspberrypi.com/software/operating-systems/#raspberry-pi-os-32-bit)
- [Raspbian 10 Buster Desktop armhf](https://www.raspberrypi.com/software/operating-systems/#raspberry-pi-os-32-bit)
- Raspbian 11 is Debian so we recommend waiting until we release Debian. Meanwhile, you can use our [Ubuntu 22.04.1](http://distro.libre.computer/ci/ubuntu/22.04/) images.

## Supported Boards
- All Libre Computer Boards

## Current Status
GPIOs, I2C, SPI, UART, PWM need to be translated via our [wiring tool](https://github.com/libre-computer-project/libretech-wiring-tool.git).
Software designed specificially for Raspberry Pi&reg; hardware will not work.
Camera, DPI screens, and DSI panels are not supported.
This is not extensively tested on all scenarios.

## How to Use
On your Raspberry Pi:registered:, run:
```bash
git clone https://github.com/libre-computer-project/libretech-raspbian-portability.git
cd libretech-raspbian-portability
sudo ./oneshot.sh aml-s905x-cc
```
Replace aml-s905x-cc with the appropriate board you want the image to run on and follow the instructions.

## Help and Support
[Libre Computer Hub](https://hub.libre.computer/t/feedback-for-raspbian-portability/32)
[Libera Chat IRC #librecomputer](https://web.libera.chat/#librecomputer)

## Roadmap
- Raspbian 11 bullseye 64-bit and 32-bit support
- Refactor to robust coding standards
- Device tree overlay translation

If you need commercial support for any distro, [please let us know](https://libre.computer/#contact).