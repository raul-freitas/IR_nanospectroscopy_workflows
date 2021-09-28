
# Workflows




The Hypespectral Image is the complex file to generate for this equipment.

There are 2 possible file types:

 - Raw files, with extension \*.gsf
 - Spectra files, with extension \*.txt

## How to open these files?

### 1. RAW files

It is the least processed file for equipment, so it is necessary to do the entire mathematical process.
There are benefits to this approach, as in this case you can have access to all measurements.
In some cases, it can be important to access SNR from all points, so with raw files you can do this.

How to open?

- To open these files you need to have **3 files in the same folder**, for example to open the second harmonic (O2)

  - "file name" O2A raw.gsf &rarr; *Interferogram of amplitude*
  - "file name" O2P raw.gsf &rarr; *Interferogram of phase*
  - "file name" .html &rarr; *File with measurement information*

- Open with ***Multifile***, when selecting the file "*[...] O2A raw.gsf*" or "*[...] O2P raw.gsf*" you need to select a specific reader, to raw files, needs to be **"*NeaSPEC raw files (\*. gsf)* "**, and the software will take care of finding the other 2 files, if they are in the same folder

- After opening the interferogram files, it is necessary to apply a Fast Fourier Transform (FFT), for that it is necessary to use the ***Interferogram to Spectrum*** widget, there are some settings available to users, such as Zero fill factor and what type of apodization you want to use. But you can just live by default if you don't want to change.

- The result of FFT is two files, "O2A" amplitude spectrum and "O2P" phase spectrum, this two files need to be splipted, for you can use them. For this you will use the ***Select Rows*** widget. Input the data from ***Interferogram to Spectrum*** in ***Select Rows***, open ***Select Rows*** and in Conditions add **channel** and type or select ***O2A***, now you have only *amplitude* spectrum in output. Put another ***Select Rows*** in data from ***Interferogram to Spectrum*** and in Conditions add **channel** and type or select ***O2P***, now you have only *phase* spectrum on another output.

- Now you have two diferent files, Phase Spectrum and Amplitude Spectrum.

### 2. Spectra files
  
It is the file generate for the equipament after Fourier Transform. In this file isn't necessary to do Fourier transform 

How to open, second harmonic?

- To open these files you need to have a unique \*.txt file.
  
  - "file name" Spectra.txt &rarr; *File with all harmonic data*

- Open with ***Multifile***, when selecting the file "*[...] Spectra.txt*" you need to select a specific reader, to Spectra .txt files, needs to be **"*NeaSPEC(\*. nea \*. txt)* "**.

- In ***Multifile*** you need to change in column: ***name***, line: *channel* ***type*** to *categorical*. It is almost the last line of the file.

- After opening the files, you need to separate the data, for you can use them. For this you will use the ***Select Rows*** widget. Input the data from ***Multifile*** in ***Select Rows***, open ***Select Rows*** and in Conditions add **channel** and type or select ***O2A***, now you have only *amplitude* spectrum in output. Put another ***Select Rows*** in data from ***Multifile***  and in Conditions add **channel** and type or select ***O2P***, now you have only *phase* spectrum on another output. 

## How to normalized these files using a reference spectrum?

 - Open the reference file following the procedure described above.

 - For normalization it is necessary to use the ***Preprocess Spectra*** widget. Input the experimental data from ***Select Rows*** in ***Preprocess Spectra***, and conect another input from reference data.
 - Open  ***Preprocess Spectra*** and click in *Add preprocessor*, select *Normalize Spectra* and check the box *Normalize by Reference* for Amplitude and *Normalize by Reference (Complex phase)* for phase.

## How to visualize?

### 1. Colormaps by position

  - In this case you need to use the ***HyperSpectra*** widget.

  - Conect the data from  ***Preprocess Spectra*** in ***HyperSpectra***.

  - Open the ***HyperSpectra*** and now you can visualized the normalized data.

  
### 2. Individual spectra by position

  - In this case you need to use the ***Spectra*** widget.

  - Conect the data from ***HyperSpectra*** in ***Spectra***.
  
  - Open the ***HyperSpectra*** and click in the position of interest.

  - Open the ***Spectra*** and now you can visualized the selected data.
