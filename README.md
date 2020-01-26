# Water Consume DataSet and Scenarios

In this repository, you'll find a dataset(consumes.csv) of simulated consumes for 9 users during the years 2018 and 2019.
The original dataset comes from this repository https://github.com/DAIAD/data/blob/master/swm_trialA.zip. This file has the following fields:

 • userId: User Id
 
 • deviceId: device Id
 
 • time: Time consume
 
 • consume: consume in liters
 
 • totalConsume: accumulated consume
 
 • isAtHome: is at home the user. This field could have the values Y(yes), N(no), U(unknow)
 
 • isAnomalous: if the consume is labeled anomalous
 
 
On the other hand, inside of the directory "scenarios" , you'll find a list of scenarios of normal and anomalous consumes. These scenarios are:

  •	Normal Consume Week (NCW)
  
  •	Normal Consume Weekend (NCWD)
  
  •	Normal Consume Night Work (NCNW)
  
  •	Normal Consume First Day (NCFD)
  
  •	Normal Consume Is At Home (NCIAH)
  
  •	Anomalous Consume Week (ACW)
  
  •	Anomalous Consume Weekend (ACWD)
  
  •	Anomalous Consume Non-Zero (ACNZ)
  
  •	Anomalous Consume Similar (ACS)
  
  •	Anomalous Consume Negative (ACN)
  
The field "wasAlertTriggered" indicates if the system should trigger or not an alert due to a leakage.
