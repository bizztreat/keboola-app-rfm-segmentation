# RFM Segmentation Application

## What It Does



## Configuration

### Parameters

<pre>
{
  "endpoint": <web-service-endpoint>
  "#apiToken": <your-secret-tocken>
  "measurementId": <your-id(s)>
  "granularity": One of these ["Base.MinuteSet", "Base.Hour", "Base.Day", "Base.Month"]
  "changedInLast": The time period for which the data will be extracted. (E.g. '30m', '24h', '7d', ...)
  "metadocuments": [true/false] If you want to also extract metadocuments for measured data
}
</pre>


- `endpoint` is an endpoint of the service
- `#apiToken` is your secret token
- `measurementId` is your unique ID(s)
- `granularity` is measured time period like minute, hour, day, ...
- `changedInLast` is time range for data extract
- `metaducuments` select if you want to read metadocuments


## Contact

BizzTreat, s.r.o
Řehořova 968/42
Prague

If you have any question contact support@bizztreat.com

Cheers!
