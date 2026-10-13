# Pressure Drop Calculator

Windows desktop application that calculates the **pressure drop (head loss)**
through a pipe run, including fittings, valves and other components.

---

## At a glance

| | |
| --- | --- |
| **Type** | Windows desktop app (WPF) |
| **Built with** | C# · .NET Framework 4.6 |
| **Status** | Stable: no recent changes (published May 2022) |

---

## Features

- **Build a pipe run** from individual items and accumulate the total head loss from per-item loss coefficients.
- **Item library:** pipe, reducer, expander, bend, mitre, converging and diverging tee, butterfly, check, stop, ball, gate, swing, globe and lift valves, entrance, exit, flange, blind flange and generic component.
- **Pipe sketch** with component symbols.
- **PCF import** (piping component files).
- **Interpolation** of loss coefficients (MathNet.Numerics).

---

## Requirements

| | |
| --- | --- |
| Operating system | Windows 10 or 11 |
| Runtime | .NET Framework **4.6** or newer |
| Build | Visual Studio 2019 or 2022 with the **.NET desktop development** workload |

---

## Building and running

1. Open `WPF_PressureDrop.sln` in Visual Studio.
2. NuGet packages restore automatically on the first build.
3. Build and run with **F5**. Sample PCF files are in `Ref/PCFs/`.

---

## Project structure

```
WPF_PressureDrop.sln
WPF_PressureDrop/
├─ HeadLossCalc.cs          head-loss model and loss coefficients
├─ Interpolation.cs         coefficient interpolation
├─ Enum*.cs, Observable.cs  binding helpers
├─ Resources/               component images and symbols
└─ MainWindow.xaml(.cs)     main window and pipe sketch
Ref/
├─ PCFs/                    sample piping component files
├─ SNVerification/          SINETZ verification examples and results
└─ Pipe_Network_Analysis.xlsx, Isogen Info.pdf   reference material
```

---

## Dependencies

| Package | Used for |
| --- | --- |
| HelixToolkit.Wpf | 3D drawing |
| MathNet.Numerics | Interpolation |
| Extended.Wpf.Toolkit (Xceed) | Data grids and docking layout |

---

## Documentation

`Ref/SNVerification` contains worked SINETZ examples (straight pipe, bend, reducer,
tee, orifice, pump curve and others) used to verify the calculation.

---

## License

Copyright © JRouss1975. All rights reserved.

No license is granted to use, copy, modify or distribute this code without written permission.
