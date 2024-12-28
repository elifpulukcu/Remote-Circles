# Remote-Circles

## Overview

Remote-Circles is a Java-based graphical application designed to generate random circles with random coordinates and radii, display them within a defined canvas, and identify the pair of circles that are the farthest apart. The application visually highlights these circles and connects them with a red line.

## Features

- **Random Circle Generation**:
  - Creates a specified number of circles with random positions and radii.
  - Ensures that all circles remain within the canvas boundaries.

- **Distance Calculation**:
  - Calculates the Euclidean distance between all pairs of circles.
  - Identifies the pair of circles that are the farthest apart.

- **Visual Representation**:
  - Draws all circles on a canvas using Java's `StdDraw` library.
  - Highlights the farthest pair of circles with thicker borders.
  - Draws a red line connecting the centers of the farthest circle pair.

- **Export**:
  - Saves the final graphical representation as an image file (`Output_figure.png`).

## Implementation Details

### Classes

#### `Circle` Class
- Represents a single circle with:
  - `x` and `y` coordinates for the center.
  - `r` for the radius.
- Methods:
  - `draw()`: Draws the circle with a standard pen radius.
  - `drawBold()`: Draws the circle with a thicker pen radius.
  - `distance(Circle c)`: Computes the Euclidean distance between two circles.

#### `Main` Class
- Handles:
  - Canvas setup.
  - Circle generation and drawing.
  - Farthest circle pair calculation.
  - Drawing a red line connecting the farthest circles.

#### `RemoteCircle` Class
- Provides an alternative implementation of the program with additional configurations for canvas size and pen radius.

### Distance Formula

The distance between two circles \( A(x_1, y_1) \) and \( B(x_2, y_2) \) is calculated as:

$$
\text{distance} = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}
$$


### Visualization
- Circles are drawn in black.
- The farthest pair of circles are drawn with a thicker border.
- A red line is drawn between their centers.

UML diagram of the Circle class is shown in Figure 2.
<p align="center">
    <img width="400" src="https://user-images.githubusercontent.com/110589752/187681321-1cb7fb18-8147-4a87-b0af-333bfa482884.png">
</p>

<h5 align="center">Figure 2. UML diagram of the Circle class</h1>

## Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/elifpulukcu/Remote-Circles.git
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd Remote-Circles
   ```

3. **Compile the Java Files**:
   ```bash
   javac *.java
   ```

4. **Run the Application**:
   ```bash
   java Main
   ```

5. **Output**:
   - A graphical window will display:
     - Generated circles.
     - The farthest circles with thicker borders.
     - A red line connecting the farthest circles.
   - The result is saved as an image file: `Output_figure.png`.

## Example Visualization

Below is an example of the application's output:
<p align="center">
    <img width="400" src="https://user-images.githubusercontent.com/110589752/187682147-33977c08-6e2c-44ef-afc3-1ffc4f3ecd1e.png">
</p>
<h5 align="center">Figure 1. Randomly generated 10 and 100 circles</h1>

## Customization

- **Number of Circles**:
  - Modify the `Circle[]` array size in the `Main` class.
  - Example: `Circle[] remoteCircles = new Circle[50];` for 50 circles.

- **Canvas Size**:
  - Modify `drawWorld()` in `Main` or `RemoteCircle` to change canvas dimensions.

- **Circle Radius Range**:
  - Update the random radius generation logic in the `Main` class.

## Prerequisites

- **Java Development Kit (JDK)**: Version 8 or higher.
- **StdDraw Library**: Ensure the `StdDraw` graphics library is available. Download it from [Princeton StdDraw Library](https://introcs.cs.princeton.edu/java/stdlib/).

## Limitations

- The application currently supports only a fixed canvas size.
- The `StdDraw` library must be preconfigured in the project environment.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Author

Developed by [Elif Pulukçu](https://github.com/elifpulukcu).







