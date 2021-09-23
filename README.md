# Orange Workflows for s-SNOM




In this repository there is some examples about how to open and post-process files from neaSNOM microscope.

The experimental data used in these examples was courtesy of FERES (2021).

------------

To download these examples click on:

   - Code;
   - Download the ZIP;
    - This will take a while, because it is a large file.
   - Select the folder and extract;
   - Open orange;
    - If you do not have orange spectroscopy installed, download [Quasar](https://quasar.codes) or [Orange](https://orangedatamining.com).
   - After running Orange, open the example;
      - File >> Open >> example
   - Now you need to indicate the file, in this example we have the filename and the reference written at the top of the orange desktop;
   - And follow the instructions...

-----------

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

 -  'F. H. Feres, R. A. Mayer, L. Wehmeier, F. C. B. Maia, E. R. Viana, A. Malachias, H. A. Bechtel, J. M. Klopf, L. M. Eng, S. C. Kehr, J. C. González, R. O. Freitas, I. D. Barcelos, Nat. Commun. 2021, 12, 1995. DOI: [10.1038/s41467-021-22209-w](https://doi.org/10.1038/s41467-021-22209-w).'