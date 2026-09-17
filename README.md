# Azigram

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22821357.svg)](https://doi.org/10.5281/zenodo.22821357)

A PAMGuard plugin that shows directional information from DIFAR sonobuoys.

The Azigram looks like a spectrogram, but colour shows the bearing of arrival in
each time-frequency cell, not its power. Weak cells fade to black, so only real
signals show clear bearings.

The plugin implements the Azigram algorithm, and frequency domain demultiplexing
of DIFAR signals, described by Thode et al. (2019).

This plugin was part of PAMGuard core until version 2.03. It is beta software.

## Requirements

- PAMGuard 2.03.00 or later.
- Multiplexed DIFAR sonobuoy data with at least 24 kHz of bandwidth.

## Installing

1. Download the jar file from the latest
   [release](https://github.com/BrianSMiller/Azigram/releases).
2. Copy it into the `plugins` folder of your PAMGuard installation.
3. Restart PAMGuard.
4. Add the module from **File > Add Module > Localisers > DIFAR Azigram Engine**.

Full instructions are in the plugin's help pages, under **Help** in PAMGuard.

## Building from source

The repository is an Eclipse project that compiles against a PAMGuard project
named `PAMGuard` in the same workspace.

1. Import both projects into Eclipse.
2. Select `src/Azigram` and choose **File > Export > Java > JAR file**.
3. Tick **Export Java source files and resources** so the help pages are
   included, and save the jar into the PAMGuard `plugins` folder.

## Citing

If you use this plugin, please cite both the plugin and the method:

Miller BS (2026). Azigram: a PAMGuard plugin for displaying directional
information from DIFAR sonobuoys. Version 0.1.0. Zenodo.
doi:10.5281/zenodo.22821357

Thode AM, Sakai T, Michalec J, Rankin S, Soldevilla MS, Martin B, Kim KH (2019).
Displaying bioacoustic directional information from sonobuoys using "azigrams".
J. Acoust. Soc. Am. 146:95-102. doi:10.1121/1.5114810

## Author

Brian Miller, Australian Antarctic Division.

## Acknowledgements

The method is that of Thode et al. (2019), cited above. Aaron Thode also shared
his MATLAB code, which helped while this implementation was being written.

## Licence

GNU General Public License v3, matching PAMGuard.
