
# A Multi-Mode Convolutional Neural Network (CNN) to reconstruct Chlorophyll-a time series in the global ocean from physical drivers

This repository is the official implementation of [A Multi-Mode Convolutional Neural Network to reconstruct
Chlorophyll-a time series in the global ocean from physical drivers](). 

## Contents
This repository contains the following PyTorch code:
- [Implementation]() of **MM-CNN** Chlorophyll-a time series regression from oceanic and atmospheric predictors 

<p align="center">
  <img src="https://github.com/JoanaR/multi-mode-CNN-pytorch/blob/main/Fig_1_method.jpg" width="650" height="300" >
</p>

## Results

Our model achieves the following performance on :

### INDIGO Dataset

| Model name         | r2  | RMSE | Slope|Seas|Inter|N param|Time computation|Km travelled by car|
| ---|--- | ---   |--- | --   |--    |--    | --             |--                 |
| ---|--- | ---   |--- | --   |--    |--    | --             |--                 |



See the paper for more details.


## Requirements
* Python Libraries :
    * PyTorch
    * Numpy
    * ...


### INDIGO Dataset - satellIte phytoplaNkton DrIvers Global Ocean
The Dataset is freely available for download [here]. 


| Proxy used as predictors         | Acroynme  | Products | spatio-Temporal Resolutions|
| ------------------ |--- | --- |--- |
| Sea Surface Temperature       | **SST** | ||
| Sea Level Anomaly      |**SLA** | ||
| Zonal and Meridional surface winds       |  **Uera, Vera** | ||
| Zonal and Meridional surface total currents     |  **u,v** |||
| Short-wave radiations      |  **SW** |||
| Binary continental mask       |  **mask** |||
| Bathymetry      |  **bathy** | ||


