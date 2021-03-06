# RTN

The code for the paper "Recurrent Translation-based Network for Top-N Sparse Sequential Recommendation."

## Requirements

We tested the code on:
* python 3.6
* pytorch 1.0.0

other requirements:
* numpy
* pandas

## Usage

Run the code using the command:
```
python main.py -d [Dataset_Name]
```
The program will automatically detect CUDA, and train the model on a GPU if possible.

The trained model will be saved in "model/[Dataset_name]/RTN.pt".

## Dataset
To use your own dataset, create csv file with filename "[Dataset_name].csv" in folder "data", where in each line is an interaction in format "[user_id],[item_id],[rating],[timestamp]".

For example, in "amz-video.csv":
```
A9RNMO9MUSMTJ,B000GIOPK2,2.0,1281052800
A2582KMXLK2P06,B000GIOPK2,5.0,1205884800
AJKWF4W7QD4NS,B000GIOPK2,3.0,1186185600
A153NZD2WZN5S3,B000GIPKWY,5.0,1273017600
...
```
Note that values of rating are unused in the program.

If a dataset contains repeatable interactions (a user interacted with an item multiple times), use option "--repeatable".