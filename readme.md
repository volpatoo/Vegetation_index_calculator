[![DOI](https://zenodo.org/badge/620394919.svg)](https://zenodo.org/badge/latestdoi/620394919)

# *Python script to perform Vegetation indices (VIs) for phenotyping*

<p align="center">
  <img src="https://github.com/msudrybeanbreeding/images/blob/main/VI_calculator/Initial_screen.png" width="70%" height="70%">
</p>

<div id="menu" />

---------------------------------------------
## Resources
  
   
   * [Online access](#P1)
   * [Disclosure](#P2)
   * [Credits](#P3)
   * [Disclaimer](#P4)
   * [Class Summary](#P5)
   * [Requirements](#P6)
   * [Installation](#Instal)
   * [Running the App](#P7)
   * [Functionalities](#P8)
   * [Pipeline](#P9)
   * [Dataset](#P10)

   * [Contact](#P21)

<div id="P1" />

---------------------------------------------
### Online access
>[**Vegetation_index_calculator**](https://msudrybeanbreeding-vegetation-index--vi-extractions-v0-3-9knpzt.streamlit.app/)
- Deployed with Streamlit app

[Menu](#menu)
<div id="P2" />
---------------------------------------------
> To run the app in a local machine, check the box. Otherwise, to use online drag or browser the data. 

<p align="center">
  <img src="https://github.com/msudrybeanbreeding/images/blob/main/VI_calculator/App_1.png" width="70%" height="70%">
</p>

> Due to software limitations, the max file size is 200 MB. To files larger than 200 MB download and deploy the app in a local machine.
---------------------------------------------
### Disclosure
> Developed and maintained by [Dr. Leonardo Volpato](https://github.com/volpatoo)

[Menu](#menu)
<div id="P3" />

---------------------------------------------
### Credits
Leonardo Volpato (volpato1@msu.edu) and Francisco Gomez (gomezfr1@msu.edu) - Michigan State University (MSU)

<div id="P4" />

---------------------------------------------

### Disclaimer

We welcome feedback and suggestions about the usefulness of the application and make no guarantee of the correctness, reliability, or utility of the results if incorrect selections are made during the steps of VIs estimation. Vegetation_index_calculator is freely accessible, and the source code will be hosted soon at [MSU Dry Bean Breeding Program GitHub page](https://github.com/msudrybeanbreeding?tab=repositories).

<div id="P5" />

---------------------------------------------
### Class Summary
> This algorithm consists in calculating vegetation indices looping through images files and plot numbers. These
indices can be used for precision agriculture for example (or remote sensing). There are functions to define the data and to calculate the
implemented indices.

#### [Vegetation index](https://en.wikipedia.org/wiki/Vegetation_Index)

A Vegetation Index (VI) is a spectral transformation of two or more bands
designed to enhance the contribution of vegetation properties and allow
reliable spatial and temporal inter-comparisons of terrestrial
photosynthetic activity and canopy structural variations

<div id="P6" />

---------------------------------------------
### Requirements

Make sure you have the following installed on your system:

- Python 3.7 or higher (https://www.python.org/downloads/)
- Streamlit (https://docs.streamlit.io/en/stable/installation.html)


<div id="Instal" />

---------------------------------------------

### Installation

1. Clone this repository or download the code as a ZIP file:

git clone https://github.com/msudrybeanbreeding/Vegetation_index_calculator.git


If you downloaded the ZIP file, extract it to a folder of your choice.

2. Change to the app directory:

cd your-repo-name

3. Install the required dependencies using pip:

pip install -r requirements.txt


It is recommended to use a virtual environment to avoid dependency conflicts with other Python projects.

<div id="P7" />

---------------------------------------------

### Running the App

To run the app, use the following command:

streamlit run VI_extractions_v0.3.py.py

The app will start, and you should see a message with the URL where you can access it, usually `http://localhost:8501`. Open the URL in your web browser to use the app.


#### Information about channels (Wavelength range for each)

* [nir - near-infrared](https://www.malvernpanalytical.com/br/products/technology/near-infrared-spectroscopy)
    Wavelength Range 700 nm to 2500 nm
    
* [Red Edge](https://en.wikipedia.org/wiki/Red_edge)
    Wavelength Range 680 nm to 730 nm
    
* [red](https://en.wikipedia.org/wiki/Color)
    Wavelength Range 635 nm to 700 nm
    
* [blue](https://en.wikipedia.org/wiki/Color)
    Wavelength Range 450 nm to 490 nm
    
* [green](https://en.wikipedia.org/wiki/Color)
    Wavelength Range 520 nm to 560 nm
    
#### Implemented index list 
> 73 in total from RGB and Multispectral (MS) sensors </p>

`abbreviationOfIndexName` -- list of channels used

            #"ARVI2"            --  red, nir
            #"CCCI"             --  red, redEdge, nir
            #"CVI"              --  red, green, nir
            #"GLI"              --  red, green, blue
            #"NDVI"             --  red, nir
            #"BNDVI"            --  blue, nir
            #"redEdgeNDVI"      --  red, redEdge
            #"GNDVI"            --  green, nir
            #"GBNDVI"           --  green, blue, nir
            #"GRNDVI"           --  red, green, nir
            #"RBNDVI"           --  red, blue, nir
            #"PNDVI"            --  red, green, blue, nir
            #"ATSAVI"           --  red, nir
            #"BWDRVI"           --  blue, nir
            #"CIgreen"          --  green, nir
            #"CIrededge"        --  redEdge, nir
            #"CI"               --  red, blue
            #"CTVI"             --  red, nir
            #"GDVI"             --  green, nir
            #"EVI"              --  red, blue, nir
            #"GEMI"             --  red, nir
            #"GOSAVI"           --  green, nir
            #"GSAVI"            --  green, nir
            #"HUE"              --  red, green, blue
            #"IPVI"             --  red, nir
            #"I"                --  red, green, blue
            #"RVI"              --  red, nir
            #"MRVI"             --  red, nir
            #"MSAVI"            --  red, nir
            #"NormG"            --  red, green, nir
            #"NormNIR"          --  red, green, nir
            #"NormR"            --  red, green, nir
            #"NGRDI"            --  red, green
            #"RI"               --  red, green
            #"IF"               --  red, green, blue
            #"DVI"              --  red, nir
            #"TVI"              --  red, nir
            #"NDRE"             --  redEdge, nir
            #"PSRI"             --  red, green, redEdge
            #"BI"               --  red, green, blue
            #"BIM"              --  red, green, blue
            #"HI"               --  red, green, blue
            #"SI"               --  red, blue
            #"VARI"             --  red, green, blue
            #"BdivG"            --  green, blue
            #"BCC"              --  red, green, blue
            #"CIVE"             --  red, green, blue
            #"COM1"             --  red, green, blue
            #"COM2"             --  red, green, blue
            #"ExG"              --  red, green, blue
            #"ExG2"             --  red, green, blue
            #"ExGR"             --  red, green, blue
            #"EXR"              --  red, green
            #"GmnB"             --  green, blue
            #"GmnR"             --  red, green
            #"GdivB"            --  green, blue
            #"GdivR"            --  red, green
            #"GCC"              --  red, green, blue
            #"MExG"             --  red, green, blue
            #"MGVRI"            --  red, green, blue
            #"NDI"              --  red, green
            #"NDRBI"            --  red, blue
            #"NGBDI"            --  green, blue
            #"RmnB"             --  red, blue
            #"RdiB"             --  red, blue
            #"RCC"              --  red, green, blue
            #"MRCCbyAlper"      --  red, green, blue
            #"RGBVI"            --  red, green, blue
            #"TGI"              --  red, green, blue
            #"VEG"              --  red, green, blue
            #"MyIndexi"         --  red, green, blue
            #"MSRGR"            --  red, green
            #"TNDGR"            --  red, green, blue

#### List of index for multispectral (MS) camera - 4 or 5 channels
 "ARVI2", "CCCI", "CVI", "NDVI", "redEdgeNDVI", "GNDVI",
 "GRNDVI", "ATSAVI", "CIgreen", "CIrededge", "CTVI", "GDVI",
 "GEMI", "GOSAVI", "GSAVI", "IPVI", "RVI", "MRVI",
 "MSAVI", "NormG", "NormNIR", "NormR", "NGRDI", "RI", "DVI",
 "TVI", "NDRE", "PSRI
 
#### List of index just with RGB channels
 "GLI", "CI", "HUE", "I", "NGRDI", "RI", "IF", 'BI','BIM',
 'HI','NGRDI','SI','VARI','BdivG','BCC','CIVE','COM1','COM2',
 'ExG','ExG2','ExGR','EXR','GmnB','GmnR','GdivB','GdivR',
 'GCC','MExG','MGVRI','NDI','NDRBI','NGBDI','RmnB',
 'RdiB','RCC','MRCCbyAlper','RGBVI','TGI','VEG','MyIndexi','MSRGR','TNDGR'

#### References
* Vegetation indices contributions from: 
[João Gustavo A. Amorim](https://github.com/TheAlgorithms/Python/blob/master/digital_image_processing/index_calculation.py)

____________________________________________________________________________________
____________________________________________________________________________________

<div id="P8" />

## Functionalities

### Left slides side:

> Before to start the running the app, the user can:
- Install or upgrade the python libraries used to perform the analysis;
- Check if the ligraries were imported correctly;
- Check the RAM available

<p align="left">
  <img src="https://github.com/msudrybeanbreeding/images/blob/main/VI_calculator/App_2.png" width="20%" height="20%">
</p>

> For all cases, a message will be displyed to inform the status to the user.

*PS: Online use, the user do not need to click on the check commands. It will be automatecly loaded by the app.*

<div id="P9" />

---------------------------------------------
## Pipeline

> An overview of the main steps to run the VIs appears in the app. 

1 - Select the data source input

2 - Input the Shapefile

3 - Select PlotID from the shp attributes

4 - Select image type - RGB or MS

5 - Image diretory Input

6 - Select VI to mask the soil

7 - Select threshold to mask the soil

8 - Run the analysis

9 - Save CSV Dataframe output

<div id="P10" />

---------------------------------------------

## Sample dataset

[RGB sample dataset and shapefile](https://github.com/msudrybeanbreeding/Suppl_files/tree/main/test_rgb) can be download here.
[MS sample dataset and shapefile] (https://github.com/msudrybeanbreeding/Suppl_files/tree/main/test_ms) also is available here.



## Runing the loop
> **j**  img numbers </p>
> **p**  plots</p>
> **i**  VIs</p>
* From the `numpy` library
> **f**  function of pixel extraction: 'mean' 'media' 'count' 'std


## Setting the image parameter to start the loop



# Saving the output into a csv table







