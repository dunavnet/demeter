### Data analytics for optimal pesticide usage

The data analytics for optimal pesticide usage is developed for four fungal diseases, as a digital model, wrapped with an API and provided as a docker container image. The component takes environmental parameters into account to quantify if conditions for a disease are met and returns recommendations on what operations to undertake on the farm to prevent the disease or to reduce its impact. 
Vineyard fungal diseases models are widely known in the agriculture. The development of sensors and IoT technology enable digitalization of these models providing timely remediation, minimizing farmers in-field effort. All models provided in this study quantify the Risk Index (RI) used to identify the need for remediation measures, that drives the decision support models provided to farmers. 
In this study, the research was based on the fact that all disease models are heavily influenced by environmental conditions such as temperature and humidity. The risk forecast models are created for four fungal diseases: 1) Downy mildew, 2) Uncinula necator (powdery mildew), 3) Guignardia bidwellii (Black rot), 4) Botrytis cinerea (grey mould) disease; and pest 5) Lobesia botrana (grapevine moth).

The APIs are composed to enable authorization process to obtain token used to POST the data to the “addmeasurement” endpoint. Data analytics for optimal pesticide usage model is expecting a specific set of data, namely temperature, humidity, precipitation and leaf wetness are required to be able to quantify the risk index and create instructions for farmers. If some of the entries are empty, model at least needs temperature or humidity to be able to provide instructions. To be able to calculate risk more efficiently, it is required to have more data values, as the accuracy of the risk will be higher. As a result, the endpoint returns instruction for the farmer

```
+----------------------------+-----------------------+-----------------------------------------------------------------------------+
|                            |                       |                                                                             |
| API name                   | Method/ Parameters    | Description                                                                 |
+----------------------------+-----------------------+-----------------------------------------------------------------------------+
|                            |                       |                                                                             |
| /Login                     | Post/                 | Returns auth token                                                          |
|                            |                       |                                                                             |
|                            | username              |                                                                             |
|                            |                       |                                                                             |
|                            | password              |                                                                             |
+----------------------------+-----------------------+-----------------------------------------------------------------------------+
|                            |                       |                                                                             |
| /agroNET/addmeasurement    | Post/                 | Post environmental parameter values to get   precipitation instructions     |
|                            |                       |                                                                             |
|                            | "date"                |                                                                             |
|                            |                       |                                                                             |
|                            | "identifier"          |                                                                             |
|                            |                       |                                                                             |
|                            |     "temperature"     |                                                                             |
|                            |                       |                                                                             |
|                            |     "humidity"        |                                                                             |
|                            |                       |                                                                             |
|                            |     "precipitation"   |                                                                             |
|                            |                       |                                                                             |
|                            |     "leafWetness"     |                                                                             |
|                            |                       |                                                                             |
|                            |     "token"           |                                                                             |
+----------------------------+-----------------------+-----------------------------------------------------------------------------+
|                            |                       |                                                                             |
| /notificationhistory       | POST/                 | List of notifications with instructions                                     |
|                            |                       |                                                                             |
|                            | MAC identifier        |                                                                             |
|                            |                       |                                                                             |
|                            | Start date            |                                                                             |
|                            |                       |                                                                             |
|                            | End data              |                                                                             |
|                            |                       |                                                                             |
|                            | Token                 |                                                                             |
|                            |                       |                                                                             |
|                            |                       |                                                                             |
+----------------------------+-----------------------+-----------------------------------------------------------------------------+

```


check API at:
https://alertnetapi.demeter.dunavnet.eu/swagger/index.html
