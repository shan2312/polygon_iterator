
# Polygon and Polygons Python Library

## Overview

This Python library provides functionality to work with regular polygons and collections of polygons. The `Polygon` class allows you to create and analyze regular polygons, while the `Polygons` class manages a collection of polygons and includes utilities for finding the most efficient polygon based on the area-to-perimeter ratio. Additionally, it includes an iterator to traverse through the collection of polygons.

## Features

- **Polygon Class**:
  - Compute geometric properties of regular polygons, such as side length, apothem, area, and perimeter.
  - Compare polygons based on vertices and circumradius.

- **Polygons Class**:
  - Manage a collection of polygons with vertex counts ranging from 3 to a specified maximum.
  - Find the most efficient polygon based on the area-to-perimeter ratio.
  - Iterate through the collection of polygons.

- **PolygonsIterator Class**:
  - Provides an iterator to traverse through the collection of polygons.

## Installation

You can integrate the code directly into your Python project. Clone this repository or copy the code into your project files.

### Cloning the Repository

```bash
git clone https://github.com/yourusername/polygon-polygons-library.git
cd polygon-polygons-library
```

## Usage

### Creating and Using Polygons

```python
from polygon_polygons_library import Polygon, Polygons

# Create a polygon with 5 vertices and circumradius 10
pentagon = Polygon(n=5, R=10)
print(pentagon)  # Output: Polygon(n=5, R=10)

# Access properties
print(f"Vertices: {pentagon.count_vertices}")
print(f"Interior Angle: {pentagon.interior_angle} degrees")
print(f"Side Length: {pentagon.side_length}")
print(f"Apothem: {pentagon.apothem}")
print(f"Area: {pentagon.area}")
print(f"Perimeter: {pentagon.perimeter}")

# Create a collection of polygons with vertices from 3 to 10, and circumradius 10
polygons = Polygons(m=10, R=10)
print(len(polygons))  # Output: 8 (polygons with 3 to 10 vertices)

# Get the maximum efficiency polygon in the collection
max_efficiency = polygons.max_efficiency_polygon
print(max_efficiency)  # Output: Polygon with the highest area-to-perimeter ratio

# Iterate through all polygons in the collection
for poly in polygons:
    print(poly)
```

## Classes

### `Polygon`

Represents a regular polygon and provides methods to compute various geometric properties.

**Constructor:**

- `__init__(self, n, R)`: Initializes a `Polygon` with `n` vertices and circumradius `R`.

**Properties:**

- `count_vertices`: Number of vertices of the polygon.
- `count_edges`: Number of edges of the polygon (same as vertices).
- `circumradius`: Circumradius of the polygon.
- `interior_angle`: Interior angle of the polygon in degrees.
- `side_length`: Length of each side of the polygon.
- `apothem`: Radius of the inscribed circle.
- `area`: Area of the polygon.
- `perimeter`: Perimeter of the polygon.

**Methods:**

- `__eq__(self, other)`: Checks equality between two `Polygon` instances based on vertices and circumradius.
- `__gt__(self, other)`: Compares two `Polygon` instances to determine if one has more vertices.

### `Polygons`

Manages a collection of polygons and provides methods for analysis and iteration.

**Constructor:**

- `__init__(self, m, R)`: Initializes a collection of polygons with vertices ranging from 3 to `m` and circumradius `R`.

**Properties:**

- `max_efficiency_polygon`: Returns the polygon with the highest area-to-perimeter ratio.

**Methods:**

- `__len__(self)`: Returns the number of polygons in the collection.
- `__iter__(self)`: Returns an iterator for the collection.
- `__getitem__(self, s)`: Retrieves the polygon at index `s` in the collection.

### `PolygonsIterator`

An iterator class for traversing through a `Polygons` collection.

**Constructor:**

- `__init__(self, polygon_obj)`: Initializes the iterator with a `Polygons` object.

**Methods:**

- `__iter__(self)`: Returns the iterator object.
- `__next__(self)`: Returns the next polygon; raises `StopIteration` when no more polygons are available.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

## Contact

For questions or feedback, please contact [shansharma23@gmail.com](mailto:shansharma23@gmail.com).

---

Thank you for using the Polygon and Polygons Python Library. We hope it enhances your geometric calculations and analysis!
```

### Summary

- **Overview**: Brief description of the library's functionality.
- **Features**: Highlights the key features of the classes.
- **Installation**: Instructions for integrating the code.
- **Usage**: Examples showing how to use the classes.
- **Classes**: Detailed descriptions of the `Polygon`, `Polygons`, and `PolygonsIterator` classes.
- **Contributing**: Guidelines for contributing to the project.
- **License**: License details.
- **Contact**: Contact information for inquiries.

Replace placeholder URLs and email addresses with your actual information. This `README.md` provides a complete overview and instructions for using the library, making it easier for others to understand and contribute.