# Aircraft Four Forces Calculator

A Python educational calculator for estimating the forces acting on an aircraft at a selected flight condition. It uses aircraft and flight inputs to calculate lift, drag, thrust, and weight, then reports derived performance values and plots how selected results change with airspeed.

## Features

- Calculates lift and drag from air density, airspeed, wing area, and aerodynamic coefficients.
- Estimates atmospheric temperature, pressure, and density from altitude.
- Calculates aircraft weight, net force, acceleration, and the lift-to-drag ratio.
- Compares lift with weight and thrust with drag to describe the approximate flight condition.
- Plots force and performance trends across a range of airspeeds, including a four-force comparison.
- Validates inputs such as aircraft mass and wing area to help prevent invalid calculations.
- Runs offline after its Python dependencies are installed.

## Inputs

The calculator is designed to accept:

| Input | Description | Typical unit |
| --- | --- | --- |
| Aircraft mass | Mass of the aircraft | kg |
| Wing area | Reference wing area | m² |
| Airspeed | Flight speed | m/s |
| Altitude | Height above sea level | m |
| Lift coefficient (`CL`) | Dimensionless lift coefficient | — |
| Drag coefficient (`CD`) | Dimensionless drag coefficient | — |
| Thrust | Engine thrust | N |

Use the units expected by the program. The table lists standard SI units; check the input prompts in the source if they differ.

## Calculations

Dynamic pressure is calculated as:

```text
q = 0.5 × ρ × V²
```

Lift and drag are then calculated as:

```text
Lift  = q × wing area × CL
Drag  = q × wing area × CD
Weight = mass × g
Net force = thrust − drag
Acceleration = net force / mass
L/D ratio = lift / drag
```

Here, `ρ` is air density, `V` is airspeed, and `g` is gravitational acceleration. The atmospheric values are estimated from altitude by the atmospheric model implemented in the program. These are educational estimates and depend on the model and assumptions used in the source.

## Requirements

- Python 3
- NumPy
- Matplotlib

Install the libraries with:

```bash
python -m pip install numpy matplotlib
```

## Run

From the folder containing the Python source, run:

```bash
python main.py
```

Replace `main.py` with the actual Python filename if it is named differently. Follow the prompts to enter the aircraft and flight parameters. The program displays the calculated atmospheric properties, forces, performance values, and flight-condition estimate, and generates the supported plots.

## Project Structure

The program is organized around these functional areas:

- Input collection and validation
- Atmospheric calculations
- Force and performance calculations
- Flight-condition analysis
- Graph generation and results display

## Interpreting Results

Lift and weight describe forces acting vertically; thrust and drag describe forces along the direction of travel. A flight-condition label is an approximation based on comparing these force pairs. Real aircraft behavior also depends on factors beyond this simplified model, such as aircraft configuration, control inputs, changing atmospheric conditions, and engine performance.

## Troubleshooting

- If Python cannot find NumPy or Matplotlib, install them using the command above in the same Python environment used to run the program.
- If a calculation is rejected, check that mass and wing area are positive and that all inputs are numeric and use the expected units.
- If a plot window does not appear, check that Matplotlib is installed and that the Python environment supports a graphical display.

## Scope

This project is intended for learning and basic estimation. It is not a flight-planning tool or a substitute for validated aircraft-performance data.
