# Uncertainty_Spatial-Temporal_Attention_Graph_Neural_Network (USTAGNN)
This code is related to the paper "Spatial-Temporal Attention Graph Neural Network with Uncertainty Estimation for Remaining Useful Life Prediction".

## Model
We proposed the model Uncertainty Spatial-Temporal Attention Graph Neural Network~(USTAGNN) for RUL prediction.

## Dataset
The experiment is based on the public data set [Turbofan Engines Degradation Simulation Data Set](https://data.nasa.gov/Aerospace/CMAPSS-Jet-Engine-Simulated-Data/ff5v-kuh6/about_data)
provided by NASA is being used in this paper for Remaining Useful Life prediction.

## File Structure
```
├───checkpoints          //To save the best model 
├───CMAPSSData           //Dataset location 
├───image                //To save the visualization result 
├───requirements.txt     //Requirements for python envoriment 
├───utils.py             //Utilities for dataset loading 
├───USTAGNN.ipynb        //Core code of USTAGNN  
└───Result               //Each result file stores the results of 10 experiments under 
                           different selections. The first line is SCORE and the second line is
                           RMSE. There are 11 columns in total, and the last column is the 
                           mean of 10 experiments.
```

## Setup
Environment setup:

```
python -m venv ./venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
python -m ipykernel install --user --name=venv
```

Download the dataset:

```
download CMAPSSData.zip 
unzip -d CMAPSSData/ CMAPSSData.zip
```

Run Code:
```
Run USTAGNN.ipynb in server

In the code there are three options to select Preprocessing Methods, Graph Construction Methods and Uncertainty Estimation Methods:
NORM_MODE = {"C-Norm", "U-Norm"}
GRAPH_MODE = {"PDAM", "IDAM", "STATIC"}
MODE = {"Dropout", "SNGP", "DUE"}
```
