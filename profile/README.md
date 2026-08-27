# P-BAN R&D Team

We are the R&D team at **P-ban.com** — 株式会社ピーバンドットコム — a
printed-circuit-board company based in Chiyoda, Tokyo. P-ban.com runs an online
service covering PCB design, fabrication and assembly, and this organization is
where we publish firmware and tooling that comes out of our own hardware work.

## gene — semi-custom development for sensor PoCs

[**gene**](https://www.p-ban.com/services/gene/) is our development service for
teams that need a working sensor demo rather than an evaluation board. A gene
Core board (40 × 40 × 20 mm, ESP32-S3 or STM32F446) pairs with a sensor module,
and we take it the whole way: schematic, PCB, assembly, firmware, and a PC
application for visualising the data.

The idea is roughly 70 % shared platform and 30 % custom, so a proof of concept
does not have to become a full-scratch engineering project. *(Service page is in
Japanese.)*

## gene + Solist-AI development kit

P-ban.com is an ecosystem partner for
[**Solist-AI™**](https://www.rohm.com/support/solist-ai), ROHM's on-device edge
AI solution, and we built a gene module around the Solist-AI microcontroller so
that inference runs on the device itself.

The **gene + Solist-AI development kit** — a no-code embedded-AI development kit
— is now on sale. It is also the kit provided to selected entrants of
[ROHM EDGE HACK CHALLENGE 2026](https://rehc.jp/), ROHM's edge-AI development
contest, which we support as a partner.

## What we publish here

### [solist_ai_iap_firmware](https://github.com/pban-rd-dev/solist_ai_iap_firmware)

The IAP (In-Application Programming) firmware pre-installed on the kit's
Solist-AI module (ROHM/Lapis ML63Q2537, Cortex-M0+). It is factory-flashed into
the top 32 KB of internal flash. On boot it brings up a UART, receives a user
firmware image over XMODEM-CRC, programs it into the application region, then
remaps and resets to boot it.

That is how kit owners replace the application firmware with their own — over a
serial cable, with no debug probe required. The repository also carries the
J-Link and OpenOCD tooling used to install the IAP itself at the factory.

### Application firmware for the kit — coming soon

The firmware that ships on the development kit will be published here shortly.
