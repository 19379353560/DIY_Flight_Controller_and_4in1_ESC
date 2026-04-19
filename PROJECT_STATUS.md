# Project Status

This repository documents a 10-layer 75A 4-in-1 ESC hardware design for FPV use.

## Available In This Repository

- Gerber manufacturing archive.
- Schematic PDF.
- PCB preview images.
- Design notes for DSHOT600, high-current routing, and Infineon gate-driver based MOSFET control.

## Validation Status

Treat this as a hardware design reference unless a specific manufacturing,
assembly, thermal, or motor-test report is documented. High-current ESC designs
need independent electrical, thermal, and layout review before ordering or use.

## Review Needed

- MOSFET gate-drive layout.
- Dead-time and shoot-through risk.
- Copper width, via current capacity, and thermal path.
- DSHOT signal integrity.
- Manufacturing checks against the Gerbers.

## Safety

LiPo batteries and high-current ESCs can cause fire, burns, or hardware damage.
Do not test with propellers attached. Start with current-limited bench testing
and verify for shorts before connecting a high-current battery.

