# Pressure Drop Calculator

WPF application that calculates pressure drop / head loss through a pipe network
including fittings, valves and other components.

## Overview

Build up a pipe run from individual items - pipe lengths, reducers, expanders,
bends, mitres, converging and diverging tees, valves, entrance and exit, flanges
- and the tool accumulates the total head loss using per-item loss coefficients.

## Features

- Item library: pipe, reducer, expander, bend, mitre, tee (converging/diverging),
  butterfly, check, stop, ball, gate, swing, globe, lift, entrance, exit, flange,
  flange blind, component
- Pipe sketch drawing and component symbols
- PCF import (piping component files)
- Interpolation helpers (MathNet.Numerics)

## Tech stack

- WPF, .NET Framework 4.6
- HelixToolkit, MathNet.Numerics

## Repository layout

```
WPF_PressureDrop/
  HeadLossCalc.cs, Interpolation.cs
  Resources/   component images and symbols
  MainWindow.xaml / .cs
Ref/
  PCFs/           sample piping component files
  SNVerification/ SINETZ verification examples and results
WPF_PressureDrop.sln
```

## Notes

The `Ref/SNVerification` folder contains worked SINETZ examples (straight pipe,
bend, reducer, tee, orifice, pump curve, ...) used to verify the calculation.
