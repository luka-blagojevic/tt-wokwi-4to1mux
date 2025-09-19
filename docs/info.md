<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

The circuit implements a 4-to-1 Multiplexer (MUX), which functions as a digitally controlled data selector. It takes four data inputs (A, B, C, D) and selects one to route to the output. The selection is controlled by two additional select line inputs (S1 and S0). The result is displayed on a single LED (Y), which will mirror the state of the chosen data input.

## How to test

The inputs can be set with the DIP switch (Select In -> Switches 1-2, Data In -> Switches 3-6). For the showcase simulation, the data inputs are connected to clock generators with frequencies of 1, 2, 4, and 8 Hz respectively. The output LED's behavior will change depending on the select line values, as shown in the function table below.

| S1 (Switch 1) | S0 (Switch 2) | Selected Data Input | Expected Output Y Behavior         |
| :-----------: | :-----------: | :-----------------: | :--------------------------------: |
|    OFF (0)    |    OFF (0)    |       A (IN2)       | Blinks **SLOWLY** (1 Hz) |
|    OFF (0)    |     ON (1)    |       B (IN3)       | Blinks **FASTER** (2 Hz) |
|     ON (1)    |    OFF (0)    |       C (IN4)       | Blinks **FAST** (4 Hz) |
|     ON (1)    |     ON (1)    |       D (IN5)       | Blinks **VERY FAST** (8 Hz) |


## External hardware

This project uses a DIP switch to provide the select line inputs. For the showcase simulation, four Clock generators (set to 1, 2, 4, and 8 Hz) are used for the data inputs, and LEDs are used to show the state of the final output.
