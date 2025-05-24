# Pressure-Depth Conversion

## Overview
This repository explores hydrostatic pressure calculations and conversions between pressure and depth in water.

The included Jupyter notebook attempts to implement basic calculations that might be helpful for estimating pressure at depth, converting between common units, and exploring practical conversion approaches based on seawater properties. The examples demonstrate both simple hydrostatic approximations and more nuanced models that account for latitude variations.

## Hydrostatic Water Pressure Formula

A commonly used approximation for hydrostatic pressure can be expressed as:

P = ρgh

Where:
- P = pressure [Pa]
- ρ = density [kg/m³]
- g = gravitational acceleration constant [m/s²]
- h = depth [m]

The notebook uses these approximate density values:
- Fresh water: 997.0474 kg/m³ (at 25°C)
- Salt water: 1023.6 kg/m³ (average value, varies with salinity and temperature)

## Practical Conversion of Pressure to Depth

For potentially more suitable pressure-to-depth conversions in seawater, the notebook explores a formula suggested in AMS Journals:

z = (1-c₁)p - c₂p²

Where:
- z = depth [m]
- p = pressure [decibars]
- c₁ = (5.92 + 5.25 sin²φ) × 10⁻³, where φ is latitude
- c₂ = 2.21 × 10⁻⁶

This formula attempts to account for some variations in seawater properties based on latitude, though it still represents a simplified model with certain limitations.



## References

- [AMS Journals | Practical conversion of pressure to depth](https://journals.ametsoc.org/view/journals/phoc/11/4/1520-0485_1981_011_0573_pcoptd_2_0_co_2.xml)
