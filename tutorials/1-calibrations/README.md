# Processing calibration frames with PyKOALA

This directory provides an introduction to users about processing calibration frames with `pykoala`.

We recommend users to first go through the set of tutorials included in `/1-calibrations`.

## Contents

### Wavelength offsets

Inaccuracies on the wavelength calibration of IFS data are not uncommon. They can originate from

- Instrumental effects. Such as flexions along the optical axis.

- Software. For example, poorly constrained wavelength solutions from arclines.

- A combination of both. For example, the light from arc lamp frames do not follow the same optical path as celestial sources.

The tutorial `wavelength_offsets.ipynb` shows how to derive an offset wavelength solution from twilight flats. See also tutorial #TODO for insrtuctions on deriving the offsets on an idividual object basis using telluric emission lines.

### Fibre throughput

TODO...

The tutorial `fibre_throughput.ipynb` illustrates how to derive fibre throuhgput sensitivity maps to correct fibre-to-fibre variations.

### Telluric absoption

The tutorial `telluric_absorption.ipynb` provies examples on how extract a telluric absorption correction.

### Spectrograph response

The tutorial `instrumental_response.ipynb` shows how to measure the wavelength-dependent spectrograph sensitivity curve using spectrophotometric standard stars.