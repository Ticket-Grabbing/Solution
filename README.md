# Dataset
## Data Source

The data disclosure process is under way, and will be updated later.


## Data Format

### user_grab_train_ticket_log.csv
The data set covers  of approximately 2 million random users from June 3, 2019 to June 3, 2022. The detailed description of the dataset is shown in the following table.

| Field | Explanation |
| --- | --- |
| User ID | An integer, the serialized ID that represents a user |
| DEP TIMESTAMP|  An integer, the serialized ID that represents the departure time |
| DEP STATION ID|  An integer, the serialized ID that represents the departure city station |
| DES STATION ID |  An integer, the serialized ID that represents the destination city station |
| TRAIN ID |  An integer, the serialized ID that represents the train number|
| ODT ID |  An integer, the serialized ID that represents the combination of the route and train number|
| ORDER TIMESTAMP|  An integer that represents the time of the pay the ticket |
| ORDER ID|  An integer, the serialized ID that represents order ID |
| IS SUCC |  An integer that represents grabbing ticket success or not, 1 represents success, 0 represents failure|
| SUCC TIMESTAMP|  An integer that represents the time of the grabbing ticket success |

### Data Preprocessing


# Prerequisites

Our code is based on Python3 (>= 3.6). There are a few dependencies to run the code. The major libraries are listed as follows:

TensorFlow (>= 1.9.0)
NumPy (>= 1.15)
SciPy (>= 1.1.0)
Pandas (>= 0.23)

# Model Details
## Training
python main.py --n_route {%num_route%} --graph {%weight_matrix.csv%}
### Folder structure

├── data_loader 
│   ├── data_utils.py 
│   └── __init__.py 
├── dataset 
│   ├── trainset.csv 
│   └── testset.csv 
├── main.py 
├── models 
│   ├── base_model.py 
│   ├── __init__.py 
│   ├── layers.py 
│   ├── tester.py 
│   └── trainer.py 
├── output 
│   ├── models 
│   └── tensorboard 
├── README.md 
└── utils 
    ├── __init__.py 
    ├── math_graph.py 
    └── math_utils.py 
