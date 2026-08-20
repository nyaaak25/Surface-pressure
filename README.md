# Data for the OMEGA/Mars Express Surface Pressure Study

## Overview

This repository contains the processed data used to generate the figures presented in the manuscript:
**Global thermal tide trends on Mars using retrieved surface pressure observed by
OMEGA/Mars Express**
by Akira Kazama et al.

This study retrieves Martian surface pressure from the 2.0 μm CO2 absorption band observed by the OMEGA imaging spectrometer onboard Mars Express. The retrieved surface pressures are used to investigate seasonal variations and diurnal thermal tides over regional-to-global scales.

This repository provides the processed numerical data directly used to generate the figures and support the analyses presented in the manuscript.
Large intermediate radiative-transfer and retrieval products are not included because of their large file sizes.

## Repository Structure
The repository is organized as follows:

```text
README.md
data/
    Figure1.txt
    Figure2_27_277.txt
    Figure2_27_MCD.txt
    Figure2_28_277.txt
    Figure2_28_MCD.txt
    Figure2_29_277.txt
    Figure2_29_MCD.txt
    Figure3_Lat_0.txt
    Figure3_Ls_180.txt
    Figure4_InSight.txt
    Figure4_OMEGA_MCD.txt
    Figure4_binned.txt
    Figure5_binned_data.txt
```

## Figure 1

`Figure1.txt`
Figure 1 shows an example OMEGA spectrum around the 2.0 μm CO2 absorption band used for the surface-pressure retrieval. The spectrum covers ~1.8–2.2 μm. Selected continuum wavelengths and the spectral range used for calculating the equivalent width are indicated in the corresponding manuscript figure.

Columns:
* Wavelength [μm]
* Radiance [W m−2 sr−1 μm−1]

The example spectrum is taken from OMEGA observation ORB0920_3.

## Figure 2

Files:
`Figure2_27_277.txt`
`Figure2_27_MCD.txt`
`Figure2_28_277.txt`
`Figure2_28_MCD.txt`
`Figure2_29_277.txt`
`Figure2_29_MCD.txt`

Figure 2 shows the seasonal variation of surface pressure retrieved from OMEGA observations for Mars Years 27, 28, and 29 and compares the retrieved pressures with the Mars Climate Database version 6.1.

The files contain:
* Solar longitude, Ls [deg]
* OMEGA-retrieved surface pressure [Pa]
* Mars Climate Database version 6.1 surface pressure [Pa]

The data correspond to the retrieval using OMEGA-derived 2.77 μm dust optical depth (_277) and MCD-predicted dust optical depth(_MCD).

## Figure 3

Files of the form:
`Figure3_Ls_0.txt`
`Figure3_Lat_180.txt`

Figure 3 shows modeled diurnal variations in Martian surface pressure predicted by the Mars Climate Database version 6.1. For files named `Figure3_Ls_180.txt`, solar longitude is fixed and latitude varies.

Columns:
* Local time [hour]
* Normalized surface-pressure variation [%]
* Latitude [deg]

For files named `Figure3_Lat_0.txt`, latitude is fixed and solar longitude varies.

Columns:
* Local time [hour]
* Normalized surface-pressure variation [%]
* Solar longitude, Ls [deg]

The normalized surface-pressure variation is defined relative to the modeled pressure at 12:00 local time.

## Figure 4
Figure 4 compares the diurnal surface-pressure variation measured by InSight with OMEGA-derived surface pressures and Mars Climate Database version 6.1 predictions.

### `Figure4_InSight.txt`

Contains the InSight pressure measurements used for the comparison.

Columns:
* Local time [hour]
* Normalized InSight surface-pressure variation [%]

### `Figure4_OMEGA_MCD.txt`

Contains individual OMEGA-derived and Mars Climate Database normalized pressure variations corresponding to the selected InSight comparison region and season.

Columns:
* Local time [hour]
* OMEGA normalized surface-pressure variation [%]
* Mars Climate Database normalized surface-pressure variation [%]

### `Figure4_binned.txt`

Contains the local-time-binned values plotted in Figure 4.

Columns:
* Local-time bin center [hour]
* Median OMEGA normalized pressure variation [%]
* Standard deviation of OMEGA normalized pressure variation [%]
* Median Mars Climate Database normalized pressure variation [%]
* Standard deviation of Mars Climate Database normalized pressure variation [%]

## Figure 5

Figure 5 presents the dependence of the diurnal surface-pressure variation on latitude, solar longitude, and local time. The analysis uses four solar-longitude intervals:

* 0°–90°
* 90°–180°
* 180°–270°
* 270°–360°

and six latitude intervals:

* 60°N–90°N
* 30°N–60°N
* 0°–30°N
* 0°–30°S
* 30°S–60°S
* 60°S–90°S

### `Figure5_binned_data.txt`

Contains the binned OMEGA and Mars Climate Database values used in Figure 5.

Columns:
* Minimum solar longitude [deg]
* Maximum solar longitude [deg]
* Minimum latitude [deg]
* Maximum latitude [deg]
* Minimum local time [hour]
* Maximum local time [hour]
* Local-time bin center [hour]
* Median OMEGA-derived pressure variation [%]
* Standard deviation of OMEGA-derived pressure variation [%]
* Median Mars Climate Database pressure variation [%]
* Standard deviation of Mars Climate Database pressure variation [%]
* Number of OMEGA observations contributing to the bin

## External Data Sources

### OMEGA / Mars Express
The original observations used in this study were obtained by the OMEGA imaging spectrometer onboard ESA's Mars Express spacecraft. The original OMEGA observations are not redistributed in this repository. They are available from the official ESA Planetary Science Archive.

### Mars Climate Database
Atmospheric temperature, pressure, and modeled surface-pressure variations used in this study were obtained from the Mars Climate Database version 6.1.

### InSight
Surface-pressure measurements from the InSight mission were used to evaluate the OMEGA-derived diurnal surface-pressure variations. The original InSight measurements are not redistributed in this repository and are available from the official mission archive described in the associated manuscript.

## Notes on Data Availability and Reproducibility
This repository contains the processed numerical values directly used to generate the figures and support the principal results of the manuscript. The original OMEGA spectra, radiative-transfer calculations, lookup tables, and large intermediate surface-pressure retrieval products are not included because of their substantially larger file sizes. These intermediate files are not required to reproduce the plotted quantities provided in this repository.
