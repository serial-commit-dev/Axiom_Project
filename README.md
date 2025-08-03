# Axiom Project (Science Fair Project)

## Overview

**Axiom Project** is a science fair project designed to demonstrate how an ultrasonic sensor can be used to control a servo motor based on distance calculations, applying the Pythagorean theorem for sensor placement and range estimation.

## How It Works

- An **HC-SR04 ultrasonic sensor** is used to measure the distance from the sensor to an object (e.g., windshield).
- The program uses the sensor reading to control a **servo motor** (e.g., opening or closing a gate).
- Sensor placement and range can be calculated using the Pythagorean theorem if the sensor is mounted above ground and offset horizontally from the target.

## Adjusting for Your Sensor

1. **Open the program file** (`Axiom_Project.ino`).
2. **Edit the variables**:  
   - `trig_pin` and `echo_pin` for your sensor wiring.
   - `max_dist` for the maximum detection range (in cm).
   - The conditional values (`Distance < 10 && Distance > 5`) to set your trigger range.
3. **Upload the program** to your Arduino-compatible board.
4. **Experiment with sensor placement**:
    - Use the formula:  
      ```
      hypotenuse = sqrt(height^2 + base^2)
      ```
    - Adjust your sensor’s height and horizontal distance to calculate the straight-line range to your target.

## Example Calculation (Pythagorean Theorem)

Suppose your sensor is **8.8 cm** above the ground and the object is **9 cm** away horizontally:
```
hypotenuse = sqrt(8.8^2 + 9^2) ≈ 12.6 cm
```
This is the distance the ultrasonic pulse travels to the object.

## How the Pythagorean Theorem Is Applied

The setup forms a right triangle:
- **Height**: vertical leg (sensor to ground)
- **Base**: horizontal leg (sensor to object)
- **Hypotenuse**: straight-line distance (sensor to object)

This calculation helps you position your sensor for accurate readings and adjust your code trigger distances.

## Credits

Created by serial-commit-dev for science fair and educational purposes.
