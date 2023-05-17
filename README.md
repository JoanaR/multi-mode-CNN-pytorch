
# A Multi-Mode Convolutional Neural Network (CNN<sub>MM</sub>) to reconstruct satellite-derived Chlorophyll-a time series in the global ocean from physical drivers

This repository contains the code of the model presented in the paper [A Multi-Mode Convolutional Neural Network to reconstruct
Chlorophyll-a time series in the global ocean from physical drivers](Frontiers in Marine Science, 2023). 

## Contents
This repository contains the following PyTorch code:
- Implementation of the multi-mode **CNN<sub>MM8</sub>** Chl time series regression from oceanic and atmospheric predictors :

<p align="center">
  <img src="https://github.com/JoanaR/multi-mode-CNN-pytorch/blob/main/Fig1.jpg" width="650" height="300" >
</p>

## Results

Our model achieves the following performance on INDIGO Benchmark dataset :

| Model name         | r<sup>2</sup>  | RMSE | Slope|Seas|Inter|N param|Time computation|Km travelled by car|
| ---|--- | ---   |--- | --   |--    |--    | --             |--                 |
| CNN<sub>MM8</sub>|0.87 | 0.28   |0.90 | 1.00   |0.96    |803 920    | 39 h             |8.9                 |


See the paper for more details.


## Requirements

### Python Libraries :

* torch==1.4.0
* torchvision==0.5.0
* numpy==1.18.1
* carbontracker==1.1.5
    
 To install the requirements libraries :
 
```
conda install -r requirements.txt
```
    
 
### INDIGO dataset download :
The benchmark formated dataset is available for download [here](https://www.seanoe.org/data/00807/91910/). You can also find the required files to run the code [in this repository] https://e.pcloud.link/publink/show?code=kZ5TyuZeuTIPNKWtsS02f60baCweJlIfwVy
This dataset was built from the following source of data :

| Proxy used as predictors         | Acronyme  | Products | Initial spatio-temporal resolutions|
| ------------------ |--- | --- |--- |
| Sea Surface Temperature       | **SST** | [Reyn_SmithOIv2 SST dataset](https://iridl.ldeo.columbia.edu/SOURCES/.NOAA/.NCEP/.EMC/.CMB/.GLOBAL/.Reyn_SmithOIv2/)  |Monthly on a 1◦ × 1◦ spatial grid|
| Sea Level Anomaly      |**SLA** |[Ssalto/Duacs merged product of CNES/SALP project]() |Weekly on a 1/3◦ × 1/3◦ spatial grid|
| Zonal and Meridional surface winds       |  **Uera, Vera** |[Atmospheric model reanalysis ERA interim 4](https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era-interim) |Every 5-days on a 0.25◦ × 0.25◦ spatial grid|
| Zonal and Meridional surface total currents     |  **u,v** |[OSCAR unfiltered satellite product](https://podaac.jpl.nasa.gov/dataset/OSCAR_L4_OC_third-deg) |Every 5-days on a 0.25◦ × 0.25◦ spatial grid|
| Short-wave radiations      |  **SW** |[NCEP/NCAR Numerical reanalysis]() |Daily on a 2◦ grid|
| Binary continental mask       |  **mask** |||
| Bathymetry      |  **bathy** | [GEBCO](https://www.gebco.net/data_and_products/gridded_bathymetry_data/gebco_2020/)|15 arc seconds|


### References

Roussillon Joana, Fablet Ronan, Gorgues Thomas, Drumetz Lucas, Littaye Jean, Martinez Elodie (2023). A Multi-Mode Convolutional Neural Network to reconstruct satellite-derived Chlorophyll-a time series in the global ocean from physical drivers. Frontiers in marine science.  doi: 10.3389/fmars.2023.1077623

Roussillon Joana, Fablet Ronan, Gorgues Thomas, Drumetz Lucas, Littaye Jean, Martinez Elodie (2022). satellIte phytoplaNkton Drivers In the Global Ocean over 1998-2015 (INDIGO Benchmark dataset). SEANOE. https://doi.org/10.17882/91910



