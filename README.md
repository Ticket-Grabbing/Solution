# Dataset
The dataset are collected at an OTP from the date 15/12/2020 to the date 15/12/2022, which covers of approximately 1652 million users' ticket-grabbing data. The detailed statistics of the dataset is shown in the following table.

![image](https://user-images.githubusercontent.com/124276774/216505465-71243d21-43d0-4bf6-a7b5-46c0d958307b.png)


## Data Source

The data and code disclosure process is under way, and will be updated later.


## Data Format
 The detailed description of the dataset is shown in the following table.
### user_grab_train_ticket_log.csv


| Field | Explanation |
| --- | --- |
| user_id | An integer, the serialized ID that represents a user |
| departure_time|  An integer that represents the timestamp of the departure time |
| departure_station|  An integer, the serialized ID that represents the departure city station |
| destination_station |  An integer, the serialized ID that represents the destination city station |
| train_number |  An integer, the serialized ID that represents the train number|
| ODT_id |  An integer, the serialized ID that represents the combination of the departure station and destination station and train number|
| pay_time|  An integer that represents the timestamp of the pay the ticket |
| order_id|  An integer, the serialized ID that represents the order ID |
| is_success |  An integer that represents grabbing ticket success or not, 1 means success while 0 means failure|
| success_time|  An integer that represents the timestamp of the grabbing ticket success |

### Data Preprocessing
All the samples are classified into two sets, i.e., 80% samples as the training set and 20% samples as the validation set. During the training phase, all the relevant data recorded before 15/11/2022 are used as the input data, and the target ticket-grabbing ticket success probability identified during the next periodical, i.e., from 16/11/2022 to 30/11/2022, are used as labels. During the testing phase, the logs from the date 01/12/2022 to the date 15/12/2022 are used as the testing data.

# Prerequisites

Our code is based on Python3 (>= 3.6). There are a few dependencies to run the code. The major libraries are listed as follows:

* TensorFlow (>= 1.9.0)
* NumPy (>= 1.15)
* SciPy (>= 1.1.0)
* Pandas (>= 0.23)

# Model Details
## Training
python main.py --model IPT --mode train
## Parameter settings:

* --model_version=IPT_base 
* --batch_size=50
* --epoch=10
* --lr=3e-2 
* --T=15 
* --T_prime=3 
* --statics_feats=True 
* --category_feats=True 
* -Dcluster="{\"worker\":{\"gpu\":100}}"
    

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
