# Orange workflows for s-SNOM nanospectroscopy data processing

In this repository you find [Orange](https://orangedatamining.com) workflows for processing s-SNOM data. An example dataset including point spectra, spectral linescan and hyperspectral mapping is provided for educational purposes. All data provided was measured with synchrotron IR broadband light sources and are a courtesy of Feres *et al.* [1].

## Guidelines for downloading and oppening workflows:

1. Go to https://github.com/raul-freitas/imbuia_workflows
2. Click on **Code** and then **Download ZIP**. This can take some time...
3. You should get the following files structure:

```
├── dataset
│   ├── hyp_dataset
│   │   ├── NF S REFERENCE hyp.html
│   │   ├── NF S REFERENCE hyp O2A raw.gsf
│   │   ├── NF S REFERENCE hyp O2P raw.gsf
│   │   ├── NF S REFERENCE hyp Spectra.txt
│   │   ├── NF S SAMPLE hyp.html
│   │   ├── NF S SAMPLE hyp O2A raw.gsf
│   │   ├── NF S SAMPLE hyp O2P raw.gsf
│   │   └── NF S SAMPLE hyp Spectra.txt
│   ├── linescan_dataset
│   │   ├── NF S REFERENCE linescan.html
│   │   ├── NF S REFERENCE linescan O2A raw.gsf
│   │   ├── NF S REFERENCE linescan O2P raw.gsf
│   │   ├── NF S REFERENCE linescan Spectra.txt
│   │   ├── NF S SAMPLE linescan.html
│   │   ├── NF S SAMPLE linescan O2A raw.gsf
│   │   ├── NF S SAMPLE linescan O2P raw.gsf
│   │   └── NF S SAMPLE linescan Spectra.txt
│   ├── point-spectrum_dataset
│   │   ├── NF S REFRENCE point-spectrum.html
│   │   ├── NF S REFRENCE point-spectrum O2A raw.gsf
│   │   ├── NF S REFRENCE point-spectrum O2P raw.gsf
│   │   ├── NF S REFRENCE point-spectrum Spectra.txt
│   │   ├── NF S SAMPLE point-spectrum.html
│   │   ├── NF S SAMPLE point-spectrum O2A raw.gsf
│   │   ├── NF S SAMPLE point-spectrum O2P raw.gsf
│   │   └── NF S SAMPLE point-spectrum Spectra.txt
│   └── README.md
├── img
│   ├── nanospectroscopy_modes.svg
│   └── README.md
├── README.md
└── workflows
│   ├── README.md
│   ├── gsf_hyperspectral_workflow.ows
│   ├── gsf_linescan_workflow.ows
│   ├── gsf_point_spectrum_workflow.ows
│   ├── txt_hyperspectral_workflow.ows
│   ├── txt_linescan_workflow.ows
│   └──txt_point_spectrum_workflow.ows
```
5. Open the Orange app (for Orange installation, access the links [Quasar](https://quasar.codes) or [Orange](https://orangedatamining.com). It is mandatory to have the **Spectroscopy** Add-On installed for this kind of data processing.);
6. Load a specific workflow based on the measurement mode, as described below.

## Broadband s-SNOM nanospectroscopy measuring modes
s-SNOM is a scanning probe ultramicroscopy modality that combines AFM and IR-visible microscopy. For the case of s-SNOM operating with broadband sources, the technique enables nanoscale spectroscopy (Figure a). As a scanning technique, it can operate point-spectral analysis (Figure b), spectral linescan (Figure c) and hyperspectral imaging (Figure d). 

<p align="center">
<img width="1200" src="img/nanospectroscopy_modes.svg"/>
<p/>

For data processing measurents from different s-SNOM modes, we provide the following Orange [workflows](workflows/) (files .ows):

 - **Point Spectrum:** a set of spectra from a single location on the sample. Recommended for local nano-spectroscopy.
 - **Spectral Linescan:** a set of point spectra acquired along a straight line. Recommended for study of interfaces.
 - **Hyperspectral Mapping:** a 2D matrix of point spectra. Recommended for multi-spectral nano-imaging cases. 

## References

[1]   F. H. Feres, R. A. Mayer, L. Wehmeier, F. C. B. Maia, E. R. Viana, A. Malachias, H. A. Bechtel, J. M. Klopf, L. M. Eng, S. C. Kehr, J. C. González, R. O. Freitas, I. D. Barcelos, Nat. Commun. 2021, 12, 1995. DOI: [10.1038/s41467-021-22209-w](https://doi.org/10.1038/s41467-021-22209-w).

