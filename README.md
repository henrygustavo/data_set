# Water Consume DataSet and Scenarios

This repository has a dataset(data_set\consumes.csv) of simulated consumes for 9 users during the years 2018 and 2019.Also, this one has 69194 records of consumption per hour, however, 
there are cases where exist less than 24 records per day.

To simulate anomalous consumption, consumption had to be updated at certain times after 2019, but the data for 2018 were not altered in order to have a historical pattern of behavior that would help us detect any anomalous behavior in 2019.The alterations were made to generate records for the anomalous scenarios and the normal high consume scenario (NHCIAH), for example, for the anomalous non-zero consume scenario (ACNZ), a random value was added to consumption that had zero, and for NHCIAH it was established that the user was within their home having a high consumption.

It's important to mention that the original dataset comes from this repository https://github.com/DAIAD/data/blob/master/swm_trialA.zip.

The dataset has the following fields:

 * id: Record Id

 * userId: User Id
 
 * deviceId: Device Id
 
 * time: Time consume (yyyy-MM-dd hh:mm:ss)
 
 * consume: Consume in liters
 
 * totalConsume: Accumulated consume
 
 * isAtHome: This field shows if the user is at home or not and could have the values Y (Yes), N (No), U (Unknown).
 
 * isAnomalous: This field labels the consume as anomalous (1) or not(0).
 
 
On the other hand, inside the directory "scenarios" exists a list of scenarios extracted from the "dataset". These scenarios are the following:

  *	Normal Consume Week (NCW): These are the hourly consumptions between Monday and Friday where there is a normal consumption of water without the presence of a leak. The file "normal_consume_week_NCW.json" belongs to this scenario and has 120 test cases.

  *	Normal Consume Weekend (NCWD): These are the hourly consumptions between Saturday and Sunday where there is normal water consumption without the presence of a leak. The file "normal_consume_weeedk_NCWD.json" belongs to this scenario and has 46 test cases.
  
  *	Normal Consume Night Work (NCNW): These are the hourly consumption on the days where a person usually does work at dawn and his water consumption is considered normal. The file "normal_consume_night_work_NCNW.json" belongs to this scenario and has 32 test cases.
  
  *	Normal Consume First Day (NCFD): Refers to hourly consumption on the first day of system use, where there should be normal consumption. The file "normal_consume_first_day_NCFD.json" belongs to this scenario and has 48 test cases.
  
  *	Normal High Consume Is At Home (NHCIAH): Consumption per hour on days where there was a high increase in water consumption, but the user is at home and is not considered an anomaly or water leak. The file "normal_high_consume_is_at_home_NHCIAH.json" belongs to this scenario and has 29 test cases.
  
  *	Anomalous High Consume Week (AHCW): These are the hourly consumptions between Monday and Friday where there is the presence of leakage due to high anomalous consumption. The file "anomalous_high_consume_week_AHCW.json" belongs to this scenario and has 85 test cases.

  *	Anomalous High Consume Weekend (AHCWD): These are the hourly consumptions between Saturday and Sunday where there is the presence of leakage due to high anomalous consumption. The file "anomalous_high_consume_weekend_AHCWD.json" belongs to this scenario and has 48 test cases.
  
  *	Anomalous Consume Non-Zero (ACNZ): These are the hourly consumptions in which during the last 24 hours in a row water consumption has not stopped registering and there is not at least one hour where consumption is zero. The file "anomalous_consume_non_zero_ACNZ.json" belongs to this scenario and has 96 test cases.
  
  *	Anomalous Consume Similar (ACS): These are the hourly consumptions where there are three consecutive consumptions with very similar values (+ -1Liter), which is considered anomalous.The file "anomalous_consume_similar_ACS.json" belongs to this scenario and has 32 test cases.
  
  *	Anomalous Consume Negative (ACN):These are the hourly consumptions in which during the last 24 hours there has been a negative trend in the accumulated consumption of water(e.g totalConsume in record ids 69192,69193) or a negative consumption has been registered.The file "anomalous_consume_negative_ACN.json" belongs to this scenario and has 68 test cases.
  
 Finally, all the test cases has the field "isAnomalous" that indicates if the system should trigger (1) or not (0) an alert due to a leakage.