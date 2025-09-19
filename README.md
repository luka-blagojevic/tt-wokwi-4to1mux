![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg) ![](../../workflows/wokwi_test/badge.svg)

# 4 to 1 Multiplexer (MUX)

## Overview

This circuit implements a 4 to 1 Multiplexer using basic 2-input logic gates in Wokwi. A MUX acts as a digital switch, selecting one of four data inputs (**A, B, C, and D**) to be routed to a single output (**Y**). The selection is controlled by two select lines (**S1 and S0**).

## Inputs

The logical inputs are mapped to the `io_in` pins of the chip, which can be controlled by a DIP switch in the simulation.

* **S1** → `IN0` (Select Line 1)
* **S0** → `IN1` (Select Line 0)
* **A** → `IN2` (Data Input A)
* **B** → `IN3` (Data Input B)
* **C** → `IN4` (Data Input C)
* **D** → `IN5` (Data Input D)

## Outputs

* **Y** → `OUT0`: Selected Data Output

## How to Use

Use the select line inputs (`IN0` and `IN1`) to choose which data channel to pass to the output. The output `OUT0` will then mirror the state of the selected data input, as described in the functional table below.

| S1 (`IN0`) | S0 (`IN1`) | Output Y is connected to... |
| :--------: | :--------: | :-------------------------: |
|     0      |     0      |     Data Input A (`IN2`)      |
|     0      |     1      |     Data Input B (`IN3`)      |
|     1      |     0      |     Data Input C (`IN4`)      |
|     1      |     1      |     Data Input D (`IN5`)      |
