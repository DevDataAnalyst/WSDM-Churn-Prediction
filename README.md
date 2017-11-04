# Kaggle WSDM Churn Prediction Challenge

## Description 
The link of the competition : https://www.kaggle.com/c/kkbox-churn-prediction-challenge 
## Theme and purpose 
KKBOX, the leading music steaming platform in Asia, is looking for a new algorthim that determines if a user will churn the subscription within 30 days after the expiry date.   
## Data Source

### train.csv
* msno: user id
* is_churn: Target value defined as whether user did not continue subscription with 30 days after expiration.

### members.csv
* msno
* city
* bd: age. 
* gender
* registered_via: registration method
* registration_init_time
* expiration_date

### transactions.csv  
* msno: user id
* payment_method_id: dummy code of payment method (range from 1 to 41, without 9)
* payment_plan_days: length of membership plan
* plan_list_price
* actual_amount_paid
* is_auto_renew
* transaction_date
* membership_expire_date
* is_cancel: whether the user canceled the membership in this transaction

### user_logs.csv
* msno: user id
* date: format %Y%m%d
* num_25: # of songs played less than 25% of the song length
* num_50: # of songs played between 25% to 50% of the song length
* num_75: # of songs played between 50% to 75% of of the song length
* num_985: # of songs played between 75% to 98.5% of the song length
* num_100: # of songs played over 98.5% of the song length
* num_unq: # of unique songs played in one day
* total_secs: total seconds played

## Evaluation 
Based on log loss model on page : https://www.kaggle.com/c/kkbox-churn-prediction-challenge#evaluation  
## Outputs 
Two columns : the first column for user ids, which can be directly approached from the datasets(excel sheets)  

the second column for a predicted probability that the user would continue the sub, value ranges from 0 to 1  

---
Version 1.2 , editted on Nov 4th, 2017 by Kyle Xie  

