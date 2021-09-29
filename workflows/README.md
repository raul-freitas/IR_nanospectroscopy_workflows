
## Workflows for processing s-SNOM data
The workflows listed above are designed to process two types of s-SNOM data files:
- **\*.gsf files**: single-channel complex interferograms (raw NeaSnom data)
- **\*.txt files**: multi-channel complex (non-normalized amplitude and phase) NeaSnom spectra

### 1. Processing raw data (\*.gsf)
To process NeaSnom raw interferograms, it is **mandatory** that the following files should be in the same folder:

```diff
└── data_folder
    ├── file name O2A raw.gsf
    ├── file name O2P raw.gsf
    └── file name.html
```
>*Files content:*
>- **O** represents **optical channel**; 
>- **2** indicates the **2nd harmonic**. Eventually, one can decide to process complex interferograms of the 3rd (O3) or 4th harmonic (O4) of the optical channel.
>- **A** and **P** represent **amplitude** and **phase**, respectively.
>- **.html** file contains the experimental parameters of the measurement (metadata).

A typical workflow for processing \*.gsf files is presented:
<p align="center">
<img width="1200" src="img/gsf_ptspec_wrkflow.svg"/>
<p/>
















### 2. Fourier processed data (\*.txt)








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
