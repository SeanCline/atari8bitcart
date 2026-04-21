# Atari 8-Bit (400/800/XL/XE) Cartridge

Atari 8-bit cartridge PCB that supports a variety of PROM configurations.

1. **Single 8 KB mode** using one 2764-compatible PROM in the right-hand socket
2. **Dual 8 KB + 8 KB mode** using two 2764-compatible PROMs.
3. **Single 16 KB mode** using one 27128-compatible PROM in the right-hand socket along with a `74AHCT1G08` for chip-enable logic.

## Hardware summary

- **U0**: can accept either:
  - a 2764-compatible (8KB) PROM for 8KB and 8KB+8KB configurations.
  - a 27128-compatible (16KB) PROM for 16KB configurations.
- **U1**: can accept a 2764-compatible (8KB) PROM only in 8KB and 8KB+8KB configurations.
- **U2**: `74AHCT1G08` single AND gate used to merge the two chip-enable lines into a single signal.
- **C0 / C1**: 100 nF bypass capacitors

## Jumper usage

The jumpers are organized into sections, one for each supported configuration.

> **Bridge only the jumpers required for the configuration you intend to use.**

## License

CERN-OHL-W-2.0

See [LICENSE.txt](LICENSE.txt)