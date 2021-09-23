# Orange workflows for s-SNOM data processing

In this repository you find Orange workflows for processing s-SNOM data. An example dataset including point spectra, spectral linescan and hyperspectral data is provided for educational purposes. All data provided was measured at a synchrotron light source and are a courtesy of F. Feres et al. [1].

## Guidlines for downloading and oppening the workflows:

1. Go to https://github.com/raul-freitas/imbuia_workflows
2. Click on **Code** and then **Download ZIP**. This can take some time...
3. Select the folder and extract;
4. Open the Orange app (for Orange installation, access the links [Quasar](https://quasar.codes) or [Orange](https://orangedatamining.com). It is mandatory to have the **Spectroscopy Add-On** installed for this kind of data processing.)
5. In the Orange app, click on **File ⇨ Open** then select the workflow (file.ows)  

   - Now you need to indicate the file, in this example we have the filename and the reference written at the top of the orange desktop;
   - And follow the instructions...

## s-SNOM files types

In this equipament is possible to generate 3 main types of data, with a better descrition of this types in this respective folders.

 - [Point Spectrum](point-spectrum/):

	This is just a spectrum measured in just one position.

	This data has a full spectrum data, wavenumber approximately 600 cm<sup>-1</sup> up to 2000 cm<sup>-1</sup>, but in only one pixel.

 - [Linescan](linescan/):

 	In this case, a full spectrum of each pixel along a path choose is during the experiment.


 - [Hyperspectral Image](hyper/):

 	In the last type is a full spectrum on each pixel inside an area.


![example image](imgs/sample_example.png)


References:

[1] - 'F. H. Feres, R. A. Mayer, L. Wehmeier, F. C. B. Maia, E. R. Viana, A. Malachias, H. A. Bechtel, J. M. Klopf, L. M. Eng, S. C. Kehr, J. C. González, R. O. Freitas, I. D. Barcelos, Nat. Commun. 2021, 12, 1995. DOI: [10.1038/s41467-021-22209-w](https://doi.org/10.1038/s41467-021-22209-w).'

[⬆ Voltar ao topo](#Orange-workflows-for-s-SNOM-data-processing)<br>
