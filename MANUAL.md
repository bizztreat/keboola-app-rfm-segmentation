# RFM Segmentation Application

## What It Does
This app compute the RFM segmentation of provided transactional data

## Configuration
Application expect exactly one input CSV file with transactions data

Application first output CSV file will be used for results of segmentation
When the option of computing business potential is selected the app expect the second output CSV file where this potential will be stored

### Parameters

<pre>
{
  "method": One of these ["quantil", "gradualQuantil", "custom"]  
  "dateFormat": Format of datetime which will be used
  "recencySegmentsCount": The recency segments count       
  "frequencySegmentsCount": The frequency segments count
  "monetarySegmentsCount": The monetary segments count
  "columns": { 
     "date": Name of date column in input file
     "price": Name of price column in input file
     "entity": Name of entity column in input file
     "cluster": Name of cluster column in input file   
  }
  "potential": One of these ["Yes", "No"]
  "thresholds": {
    "recency": Array of recency thresholds
    "frequency": Array of frequency thresholds
    "monetary": Array of monetary thresholds
  }
}
</pre>

- `method` Define the method used for segmentation
- `dateFormat` Define the format of datetime of input and also the output 
- `recencySegmentsCount` Define the recency segments count when quantil or gradualQuantil method of segmentation is used
- `frequencySegmentsCount` Define the frequency segments count when quantil or gradualQuantil method of segmentation is used
- `monetarySegmentsCount` Define the monetary segments count when quantil or gradualQuantil method of segmentation is used
- `columns` Define the name of columns in input file
  - `date` Define the name of date column in input file
  - `price` Define the name of price column in input file
  - `entity` Define the name of entity column in input file (typicaly the userdId)
  - `cluster` Define the name of cluster column in input file, when the data are not clustered leaved it empty
- `potential` Define whether the business potentila should be computed
- `thresholds` Define the thresholds for segments when custom method is used

Method specification:
  - `Custom` User will define the segments thresholds himself
  - `Quantil` User will define the number of segments. Entitis's values at the thresholds of quantils will be used as thresholds for segments
  - `GradualQuantil` Same as Quantil but thresholds for segments are computed gradually to avoid the situation where there are the big group that is spread over multiple segments which will cause to these segments to be empty.
  
## Contact

BizzTreat, s.r.o
Řehořova 968/42
Prague

If you have any question contact support@bizztreat.com

Cheers!
