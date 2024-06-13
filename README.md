# PyKOALA Tutorials (UNDER CONSTRUCTION)

----

Welcome to the `pykoala-tutorials` repository! This repository is designed to provide a comprehensive set of tutorials to help you get started with the `pykoala` Python library. `pykoala` is a powerful tool for performing data reduction and manipulation tasks with integral field spectroscopic data.

## Table of Contents

- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Tutorials](#tutorials)
  - [Basic Tutorial 1: The philosophy of pykoala](#basic-tutorial-1-the-philosophy-of-pykoala)
  - [Basic Tutorial 2: Loading and Inspecting Data](#basic-tutorial-2-loading-and-inspecting-data)
  - [Intermediate Tutorial 1: Processing Fibre flats](#intermediate-tutorial-1-processing-fibre-flats)
  - [Intermediate Tutorial 2: Processing Standard stars](#intermediate-tutorial-2-processing-standard-stars)
  - [Intermediate Tutorial 3: Producing scientific data](#intermediate-tutorial-3-producing-scientific-data)
  - [Advanced Tutorial 1: Sky substraction](#advanced-tutorial-1-sky-substraction)
  - [Advanced Tutorial 2: Data cube interpolation methods](#advanced-tutorial-2-data-cube-interpolation-methods)
  - [Advanced Tutorial 3: Improving the astrometry with external data](#advanced-tutorial-3-improving-the-astrometry-with-external-data)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

The `pykoala` library is designed to facilitate the processing and analysis of integral field spectroscopic (IFS) data. These data are essential in various fields of astronomy and astrophysics, providing spatially resolved spectra that allow for detailed studies of astronomical objects.

This repository contains a series of tutorials aimed at demonstrating how to effectively use `pykoala` to handle IFS data. Each tutorial focuses on different aspects of the data reduction and analysis process, from basic setup to advanced spectral analysis and visualization techniques.

## Getting Started

To get started with the tutorials, you will need to have `pykoala` installed on your system. Detailed installation instructions can be found in the [documentation page](https://pykoala.readthedocs.io/en/latest/index.html), or in the Github [repository](https://github.com/pykoala/pykoala).

### Cloning the Repository

To clone this repository and get access to all the tutorials, use the following command:

```sh
git clone https://github.com/pykoala/pykoala-tutorials.git
cd pykoala-tutorials
```

### Prerequisites

- Python 3.7 or higher
- `pykoala` library
- Additional dependencies as listed in each tutorial

## Tutorials

### Basic Tutorial 1: The philosophy of pykoala

In this tutorial you will be introduced to the architecture of the library and its
current capabilities.

### Basic Tutorial 2: Loading and Inspecting Data

Understand how to load integral field spectroscopic data, either Row Stacked Spectra (RSS) or 3D datacubes, using `pykoala` and perform basic inspections to ensure data quality.

### Intermediate Tutorial 1: Processing Fibre flats

Learn the basic steps for computing the fibre throughput using flat frames.

### Intermediate Tutorial 2: Processing Standard stars

Learn how to process observations of standard stars and extract the spectral response of the spectrograph for calibrating the flux of your data.

### Intermediate Tutorial 3: Producing scientific data (from RSS to Cubes)

Explore the basic steps for combining RSS data into a Data cube.

### Advanced Tutorial 1: Sky substraction

### Advanced Tutorial 2: Data cube interpolation methods

### Advanced Tutorial 3: Improving the astrometry with external data


## Contributing

We welcome contributions to enhance the tutorials and the `pykoala` library. If you would like to contribute, please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a pull request

Please make sure to update tests as appropriate.

## License

This project is licensed under the BSD 3-Clause License - see the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions, suggestions, or feedback, feel free to open an issue or contact the maintainers directly.

Happy coding and exploring the universe with `pykoala`!

