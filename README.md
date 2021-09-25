# Orange workflows for s-SNOM nanospectroscopy data processing

In this repository you find Orange workflows for processing s-SNOM data. An example dataset including point spectra, spectral linescan and hyperspectral data is provided for educational purposes. All data provided was measured at a synchrotron light source and are a courtesy of Feres *et al.* [1].

## Guidlines for downloading and oppening workflows:

1. Go to https://github.com/raul-freitas/imbuia_workflows
2. Click on **Code** and then **Download ZIP**. This can take some time...
3. Select the folder and extract;
4. Open the Orange app (for Orange installation, access the links [Quasar](https://quasar.codes) or [Orange](https://orangedatamining.com). It is mandatory to have the **Spectroscopy** Add-On installed for this kind of data processing.);

## Broadband s-SNOM nanospectroscopy measuring modes
s-SNOM is a scanning probe ultramicroscopy modality that combines AFM and IR-visible microscopy. For the case of s-SNOM operating with broadband sources, the technique enables nanoscale spectroscopy (Figure a). As a scanning technique, it can operate point-spectral analysis (Figure b), spectral linescan (Figure c) and hyperspectral imaging (Figure d). 

<p align="center">
<img width="1200" src="img/nanospectroscopy_modes.svg"/>
<p/>

For data processing of measurents of different s-SNOM modes, we provide the following Orange workflows (files.ows):

 - [Point Spectrum](point_spectrum/)

 - [Spectral Linescan](spectral_linescan/)

 - [Hyperspectral Mapping](hyperspectral_map/)

References:
[1] F. H. Feres, R. A. Mayer, L. Wehmeier, F. C. B. Maia, E. R. Viana, A. Malachias, H. A. Bechtel, J. M. Klopf, L. M. Eng, S. C. Kehr, J. C. González, R. O. Freitas, I. D. Barcelos, Nat. Commun. 2021, 12, 1995. DOI: [10.1038/s41467-021-22209-w](https://doi.org/10.1038/s41467-021-22209-w).

