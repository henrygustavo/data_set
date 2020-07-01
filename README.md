# Water Consume DataSet and Scenarios

In this repository, you'll find a dataset(consumes.csv) of simulated consumes for 9 users during the years 2018 and 2019.This dataset has 69194 records of consumption per hour. The original dataset comes from this repository https://github.com/DAIAD/data/blob/master/swm_trialA.zip. This file is inside the directory data_set and has the following fields:

 * id: Record Id

 * userId: User Id
 
 * deviceId: Device Id
 
 * time: Time consume (yyyy-MM-dd hh:mm:ss)
 
 * consume: Consume in liters
 
 * totalConsume: Accumulated consume
 
 * isAtHome: This field shows if the user is at home or not and could have the values Y (Yes), N (No), U (Unknown).
 
 * isAnomalous: This field labels the consume as anomalous or not.
 
 
On the other hand, inside of the directory "scenarios", you'll find a list of scenarios extracted from the dataset with their test cases of normal and anomalous consumes. These scenarios are:

  *	Normal Consume Week (NCW): These are the consumes per hour between monday and friday where there is a normal consumption of water without the presence of leakage. The file "normal_consume_week_NCW.json" belongs to this scenario and has 120 test cases.

  *	Normal Consume Weekend (NCWD): These are the consumes per hour between Saturdary and sunday where there is a normal consumption of water without the presence of leakage. The file "normal_consume_weeedk_NCWD.json" belongs to this scenario and has 46 test cases.
  
  *	Normal Consume Night Work (NCNW): These are the consumes per hour on the days where a person usually does work during the early morning and their water consumption is considered normal. The file "normal_consume_night_work_NCNW.json" belongs to this scenario and has 32 test cases.
  
  *	Normal Consume First Day (NCFD): Refers to the consumes per hour of the first day of use of the system, where there should be normal consumption. The file "normal_consume_first_day_NCFD.json" belongs to this scenario and has 48 test cases.
  
  *	Normal High Consume Is At Home (NHCIAH): These are the consumes per hour on the days when there was a high increase in water consumption, but the user is at home and is not considered an anomaly or water leak. The file "normal_high_consume_is_at_home_NHCIAH.json" belongs to this scenario and has 29 test cases.
  
  *	Anomalous High Consume Week (AHCW): These are the consumes per hour between monday and friday where there is a leak due to anomalous consumption The file "anomalous_high_consume_week_AHCW.json" belongs to this scenario and has 85 test cases.

  *	Anomalous High Consume Weekend (AHCWD): These are the consumes per hour between saturday and Sunday where there is a leak due to anomalous consumption The file "anomalous_high_consume_weekend_AHCWD.json" belongs to this scenario and has 48 test cases.
  
  *	Anomalous Consume Non-Zero (ACNZ): These are the consumes per hour on the days in which during the last 24 hours in a row the water consumption has not stopped registering and there is not at least one hour where the consumption is zero. The file "anomalous_consume_non_zero_ACNZ.json" belongs to this scenario and has 100 test cases.
  
  *	Anomalous Consume Similar (ACS): These are the consumes per hour on the days when there are three consecutive consumption with very similar values (+ -1Liter), which is considered anomalous.The file "anomalous_consume_similar_ACS.json" belongs to this scenario and has 32 test cases.
  
  *	Anomalous Consume Negative (ACN): These are the consumes per hour on the days on which during the last 24 hours there has been a negative trend in the accumulated consumption of water or a negative consumption has been recorded.The file "anomalous_consume_negative_ACN.json" belongs to this scenario and has 68 test cases.

Finally, All the test cases has the field "isAnomalous" and indicates if the system should trigger (1) or not (2) an alert due to a leakage.