
[![DOI](https://zenodo.org/badge/620394919.svg)](https://zenodo.org/badge/latestdoi/620394919)

# *Python script to perform Vegetation indices (VIs) for phenotyping*

<p align="center">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/Initial_screen.png" width="70%" height="70%">
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
   * [Shapefile](#P11)
   * [Select image features](#P12)
   * [Input image data](#P13)
   * [Masking soil](#P14)
   * [VIs list available](#P15)
   * [Running VIs analysis](#P16)

<div id="P1" />

---------------------------------------------
### Online access
>[**Vegetation_index_calculator**](https://msudrybeanbreeding-vegetation-index--vi-extractions-v0-3-9knpzt.streamlit.app/)
- Deployed with Streamlit app


<div id="P2" />

> To run the app in a local machine, check the box. Otherwise, to use online drag or browser the data. 

<p align="center">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_1.png" width="70%" height="70%">
</p>

> Due to software limitations, the max file size is 200 MB. To files larger than 200 MB download and deploy the app in a local machine.
---------------------------------------------
### Disclosure
> Developed and maintained by [Dr. Leonardo Volpato](https://github.com/volpatoo)


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

[Menu](#menu)
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

[Menu](#menu)
<div id="P8" />

## Functionalities

### Left slides side:

> Before to start the running the app, the user can:
- Install or upgrade the python libraries used to perform the analysis;
- Check if the ligraries were imported correctly;
- Check the RAM available

<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_2.png" width="20%" height="20%">
</p>

> For all cases, a message will be displyed to inform the status to the user.

*PS: Online use, the user do not need to click on the check commands. It will be automatecly loaded by the app.*

[Menu](#menu)
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

[Menu](#menu)
<div id="P10" />

---------------------------------------------

## Sample dataset

- [RGB sample dataset and shapefile](https://github.com/msudrybeanbreeding/Suppl_files/tree/main/test_rgb) can be download here.

- [MS sample dataset and shapefile](https://github.com/msudrybeanbreeding/Suppl_files/tree/main/test_ms) also is available here.

[Menu](#menu)
<div id="P11" />

---------------------------------------------
## Shapefile input

<p align="center">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_4.png" width="70%" height="70%">
</p>

> Once the shapefile is uploaded, the user will be able to visualize the first line of the shapefile features.
> Then, the user needs to select the "select field name" to identify the plot ID which will be used in the loop and in the final data table results. 

- Only shp. files format are accepted;
- Zip folder should be used when online running.

> A message will display to the user if the shapefile was uploaded correctly:

<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_5.png" width="30%" height="30%">
</p>

> The plot ID name selected also will be displayed in the app:

<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_6.png" width="20%" height="20%">
</p>

[Menu](#menu)
<div id="P12" />

---------------------------------------------
## Select the image features

> The user has the option to choose between **RGB** and **MS** image data.

 - [x] RGB

<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_10.png" width="40%" height="40%">
</p>

 - [x] Multispectral - MS

<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_7.png" width="30%" height="40%">
</p>

[Menu](#menu)
<div id="P13" />

---------------------------------------------
## Orthomosaic or Reflectance map inputs

 - The user can only input files in the .TIF format.
 - In order to comply with software limitations, 200MB per file is limited when used online.
 - File size is not limited to local machine use. 

> A list of file names will appear once upload has been successfully completed.

**RGB data**
<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_11.png" width="52%" height="52%">
</p>

**MS data**
<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_12.png" width="40%" height="40%">
</p>

- The user will need to provide the correct number of reflectance bands used to perform the analysis. 

> For local machine use, the user must provide the path containing either the Orthomosaic (RGB data) or Reflectance maps (MS data). Otherwise, an error message will appear.
<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_13.png" width="35%" height="30%">
</p>

[Menu](#menu)
<div id="P14" />

---------------------------------------------
## Masking the ground
The soil can be removed by creating a VI index mask. 
The user can select a particular VI in a list and its respective threshold

<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_14.png" width="35%" height="35%">
</p>

[Menu](#menu)
<div id="P15" />

---------------------------------------------
## Vegetation index to run
The list to RGB or MS data (depending on the user data selection) will be displayed.

The user can choose to run using the complete list:
<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_15.png" width="90%" height="80%">
</p>

<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_17.png" width="90%" height="80%">
</p>

Or select a specific VI to run the analysis:
<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_14.png" width="35%" height="50%">
</p>

[Menu](#menu)
<div id="P16" />

---------------------------------------------
## Running the VIs analysis  

>Once all input and settings have been completed by the user, the button "Run Vis" will be enabled. Otherwise, an error message will be displayed:
 
<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_18.png" width="35%" height="35%">
</p>

Troubleshooting can include:
- Upload correct image format (.TIF);
- Select the correspondent data to run according to the image data
	- RGB ***image type*** has to be selected when inputting an orthomosaic; or
	- MS ***image type*** when input reflectance maps.
	- Remove the spaces (if any) from the image file names.
	- Shapefile format (.shp).
	- Shapefile metric units (Shapefile has to need the CRS from image data).

### Run botton
> Once the Run VIs button is displayed, the use will be able to see the file name to be saved:
> 
<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_19.png" width="35%" height="35%">
</p>

### Runing the loop
The batch process passing through:
> **j**:  img numbers 
> **p**:  plots
> **i**:  VIs
> **f**:  function of pixel extraction: 'mean', 'media', 'count', and 'std

###  Saving the output into a csv table

Once the loop completion, a success message will be displayed as well as a table containing the results for each image data, plot ID (row) and VIs, and method extraction (column). 
- Finally, the user can download the output by clicking on the "*Download CSV file*" button. 

<p align="left">
  <img src="https://raw.githubusercontent.com/msudrybeanbreeding/images/main/VI_calculator/App_20.png" width="100%" height="50%">
</p>







