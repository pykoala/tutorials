# PyKOALA Tutorials

----

Welcome to the `pykoala-tutorials` repository! This repository is designed to provide a comprehensive set of tutorials to help you get started with the `pykoala` Python library. `pykoala` is a powerful tool for performing data reduction and manipulation tasks with integral field spectroscopic data.

## Table of Contents

- [Introduction](#introduction)
  - [A brief summary of IFS data reduction](#a-brief-recap-on-ifs-data-reduction)
  - [What's included in PyKOALA](#whats-included-in-pykoala)
- [Getting Started](#getting-started)
- [Tutorials](#tutorials)
  - [Getting Up to Speed](#getting-up-to-speed)
  - [Advanced Tutorials](#advanced-tutorials)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

# Introduction

The `pykoala` library is designed to facilitate the processing and analysis of integral field spectroscopic (IFS) data. These data are essential in various fields of astronomy and astrophysics, providing spatially resolved spectra that allow for detailed studies of astronomical objects.

## A brief summary of IFS data reduction

Reducing IFS data involves several steps to ensure that the raw data are transformed into scientifically useful spectra. Here is an outline of these steps:

1. **Raw exposures preprocessing**
  
    **a**. *Bad pixels*: identify and remove/flag cosmic ray hits or bad pixels from the frames.

    **b**. *Bias Subtraction*: remove the electronic noise by subtracting the bias frame from all science and calibration frames.

    **c**. *Dark Subtraction*: remove the thermal noise by subtracting the dark frame from all science and calibration frames.

    **d**. *Flat Field Correction*: correct for pixel-to-pixel sensitivity variations by dividing the science frames by a (detector) flat field frame.

2. **Fiber (Tramline) Extraction**

    Identify and extract individual fiber spectra from the raw exposures. This involves mapping the detector pixels to specific fibers based on the instrument's layout, usually using a trace solution derived from a fiber flat field or a dedicated tramline map.

    The resulting product is the so-called *Raw Stacked Spectra* (RSS) containing the individual spectra of each fibre.

2. **Wavelength Calibration**

    **a**. *Arc Lamp Calibration*: use arc lamp RSS spectra to identify known emission lines and create a wavelength solution.

    **b**. *Sky Line Calibration*: fine-tune the wavelength calibration using sky emission lines, if available.

3. **Fiber Throughput**

    **a**. *Fiber Throughput Correction*: correct for variations in fiber throughput by comparing the relative intensities of a uniformly illuminated source: e.g. a dome/twilight flat exposure or a selection of sky emission lines (estimated for each invidual frame).

4. **Atmospheric effects**

    **a**. *Sky Emission Subtraction*: subtract the sky emission by using dedicated sky frames, sky fibres or by identifying sky-dominated regions within the field of view.

    **b**. *Telluric Absorption Correction*: observe a telluric standard star or use an atmospheric model (e.g. Molecfit) to correct for absorption features introduced by the Earth's atmosphere.

    **c**. *Atmospheric Extinction Correction*: correct for atmospheric extinction using the standard star observation or a model of the atmospheric extinction.

5. **Flux Calibration**

    **a**. *Spectrograph Response Function*: use observations of standard stars with known spectral energy distribution to calibrate the spectrograph walenght-dependent sensitivity function.

6. **Astrometry Correction**

    **a** *RSS frames registration*: estimate the astrometric offset between individual RSS exposures by cross-correlating them or using external ancillary data.

    **b** *Absolute Astrometric Calibration*: if required, use reference catalogs to provide an absolute calibration.

7. **Data Cube Construction**

    **a**. *Combine Individual RSS Exposures*: combine multiple exposures of the same target into a 3D data cube. This is essential for:
    
      - Increasing the signal-to-noise ratio
      - Removing cosmic rays / outliers
      - Accounting for gaps between fibres of individual exposures and improve spatial sampling.

8. **Final Calibration**

    **a**. Final Flux Calibration: apply the final flux calibration to the entire data cube using the observed standard stars.

9. **Quality Assessment**

    **a**. Check for Artifacts: inspect the data cube for any residual artifacts, such as imperfect sky subtraction or cosmic ray hits.

    **b**. Signal-to-Noise Ratio: evaluate the signal-to-noise ratio across the field and spectrum to ensure data quality.

## What's included in PyKOALA

Currently, the entry point of `pykoala` are wavelength-calibrated Raw Stacked Spectra (RSS) data, althought the wavelength calibration accuracy doesn't need to be perfect, since `pykoala` includes tools for correcting fibre-to-fibre wavelength offsets.

The library provides processing tools covering points [2-9] of the previous [section](#a-brief-summary-of-ifs-data-reduction):

- Wavelength offset corrections
- Fibre throughput
- Atmospheric corrections (sky emission, telluric absorption and atmospheric extinction)
- Flux calibration using standard stars
- Astrometric calibrations either relative or absolute (using external data)
- Data cube interpolation
- Quality control visualization tools

# Tutorials

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

- Python 3.8 or higher
- `pykoala` library
- Additional dependencies as listed in each tutorial

## Outline of the tutorials

### A beginner's guide to PyKOALA

We provide a comprehensive guide to pykoala's utilities, helping users prepare for reducing their own data. The guide is divided into three main sections:

- [Introduction](tutorials/0-introduction/README.md)

  This section covers the basic concepts of the library, including the main classes and architecture, I/O features, verbosity, and logging facilities.

- [Calibrations](tutorials/1-calibrations/README.md)

  Learn how to process calibration exposures, which are essential for reducing science data.

- [Science data](tutorials/2-science-data/README.md)

  Detailed instructions on how to reduce science frames, turning RSS data into scientifically useful results.

We highly recommend following the tutorials in the specified order. Each tutorial builds on the previous ones, using products or features derived from earlier steps without re-explanation.

### Advanced tutorials

Some algorithms or techniques are complicated, and might turn more difficult to use. These tutorials aim to go one step further and delve deep into the use of advanced DR functions.

### Advanced Tutorial 1: Sky substraction techniques

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

