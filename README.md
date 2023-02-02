# Data Source



# Data Format

### user_grab_train_ticket_log.csv
The data set covers  of approximately 2 million random users from June 3, 2019 to June 3, 2021. The organization of the data set is similar to MovieLens-20M, namely Each row of the collection represents a user data behavior, which is composed of user ID, product ID, behavior type, and log. Each column summarizes the detailed information of the product under investigation.
| Field | Explanation |
| --- | --- |
| User ID | An integer, the serialized ID that represents a user |
| DEP STATION ID|  An integer, the serialized ID that represents a separture city station |
| ARR STATION ID |  An integer, the serialized ID that represents an arrive city station |
| DEP TIMESTAMP|  An integer, the serialized ID that represents departure time |
| ODT ID |  An integer, the serialized ID that represents the combination of the route and train number|
| ORDER TIMESTAMP|  An integer that represents the time of the pay the ticket |
| ORDER ID|  An integer, the serialized ID that represents order ID |
| IS SUCC |  An integer that represents grabbing ticket success or not, 1 represents success, 0 represents failure|
| SUCC TIMESTAMP|  An integer that represents the time of the grabbing ticket success |

