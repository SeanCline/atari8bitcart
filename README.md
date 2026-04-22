# Cartridge for 8-Bit Atari Computers (400/800/XL/XE)

[![Build Gerbers](https://github.com/SeanCline/atari8bitcart/actions/workflows/build-gerbers.yml/badge.svg)](https://github.com/SeanCline/atari8bitcart/actions/workflows/build-gerbers.yml)

Configurable Atari 8-bit cartridge PCB for the Atari 400/800/XL/XE line of home computers.

1. **Single 8 KB mode** using one 2764-compatible PROM in the right-hand socket.
2. **Dual 8 KB + 8 KB mode** using two 2764-compatible PROMs.
3. **Single 16 KB mode** using one 27128-compatible PROM in the right-hand socket along with a `74AHCT1G08` for chip-enable logic.

## Hardware Summary

- **U0**: accepts either:
  - a 2764-compatible (8 KB) PROM for 8 KB and 8 KB + 8 KB configurations.
  - a 27128-compatible (16 KB) PROM for 16 KB configurations.
- **U1**: accepts a 2764-compatible (8 KB) PROM in 8 KB and 8 KB + 8 KB configurations.
- **U2**: `74AHCT1G08` single AND gate used to merge the two chip-enable lines (/S4 and /S5) into a single signal.
- **C0 / C1**: 100 nF bypass capacitors.

## Jumper Configuration

The jumpers are organized into sections, one for each supported configuration.

> ℹ️ **Bridge only the jumpers required for the configuration you intend to use.**

## Releases

The latest gerber files can be found in the build artifacts of this repository.
At the moment, the gerbers are generated for JLCPCB, but it should be pretty easy to send them to a PCB fab of your choosing.

## License

CERN-OHL-W-2.0

See [LICENSE.txt](LICENSE.txt).

---

**Trademark notice:** Atari is a trademark of its respective owner. This project is an independent, unofficial hardware design and is not affiliated with or endorsed by Atari.
