# Dataset
The dataset are collected at an OTP from the date 15/12/2020 to the date 15/12/2022, which covers of approximately 3.52 million users' ticket-grabbing data. The detailed statistics of the dataset is shown in the following table.

![image](https://user-images.githubusercontent.com/124276774/216505465-71243d21-43d0-4bf6-a7b5-46c0d958307b.png)


## Data Source

The data and code disclosure process is under way, and will be updated later.


## Data Format
 The detailed description of the dataset is shown in the following table.
### user_grab_train_ticket_log.csv


| Field | Explanation |
| --- | --- |
| User ID | An integer, the serialized ID that represents a user |
| DEP TIMESTAMP|  An integer that represents the timestamp of the departure time |
| DEP STATION ID|  An integer, the serialized ID that represents the departure city station |
| DES STATION ID |  An integer, the serialized ID that represents the destination city station |
| TRAIN ID |  An integer, the serialized ID that represents the train number|
| ODT ID |  An integer, the serialized ID that represents the combination of the departure station and destination station and train number|
| ORDER TIMESTAMP|  An integer that represents the timestamp of the pay the ticket |
| ORDER ID|  An integer, the serialized ID that represents the order ID |
| IS SUCC |  An integer that represents grabbing ticket success or not, 1 means success while 0 means failure|
| SUCC TIMESTAMP|  An integer that represents the timestamp of the grabbing ticket success |

### Data Preprocessing


# Prerequisites

Our code is based on Python3 (>= 3.6). There are a few dependencies to run the code. The major libraries are listed as follows:

* TensorFlow (>= 1.9.0)
* NumPy (>= 1.15)
* SciPy (>= 1.1.0)
* Pandas (>= 0.23)

# Model Details
## Training
python main.py --model IPT --mode train
### Folder structure

```
├── README.md
├── dataset
│   ├── train_dataset.csv
│   └── vilidation_dataset.csv
│   └── test_dataset.csv
├── main.py
├── models
│   ├── model_fun.py
│   ├── __init__.py
│   ├── layers.py
│   ├── tester.py
│   └── trainer.py
├── output
│   ├── models
│   └── tensorboard
├── data_loader
│   ├── data_utils.py
│   └── __init__.py
└── utils
    ├── __init__.py
    ├── graph_utils.py
    └── my_utils.py
    

```
