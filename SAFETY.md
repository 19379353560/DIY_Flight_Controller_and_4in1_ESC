# Safety

This repository contains high-current ESC hardware files. Treat the design as
experimental and under review until independently verified.

## Before Manufacturing

- Review the schematic, Gerbers, layer stack, copper paths, and connector
  assumptions.
- Check MOSFET, gate-driver, bootstrap, DSHOT, and current-return routing.
- Confirm component ratings and thermal assumptions.

## Before Power

- Use current-limited bench power.
- Do not connect propellers during bench tests.
- Start with low voltage and no-load checks.
- Stop immediately if any component overheats, draws unexpected current, or
  behaves unpredictably.

## Reporting Issues

For power electronics review, use:

https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC/issues/1

For discussion, use:

https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC/discussions/2
