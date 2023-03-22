### Description
The component provides the table with a list of drivers and list of machines with details about the driver behavior, machine distance covered and vehicle average speed. The components receive data about latitude, longitude, speed, braking and fuels consumption as input in the  DEMETER  AIM  format.  These data are then analyzed, and the output of the classification process is then provided to the dashboard output including the data about the users’ behavior, distance covered and average speed. The component is generic and with slight adaptation can be employed in any use cases involving transport, where it is necessary to monitor the driver behavior, or the performance of the vehicles (for low fuel consumption, high-risk and sensitive merchandise, etc.).

### Deployment details 

To start API first login to container registry:
```
sudo docker login demeter.azurecr.io
user: demeter
pass: Please send a request to info@dunavnet.eu to receive a password 

```
Start API container:
```
sudo docker-compose pull
sudo docker-compose up -d
```

check API at:
http://localhost:8001/swagger/index.html


### Screenshots
 
[Image 1 – Knowage dashboard for Field operation component](https://sasagronet.blob.core.windows.net/demeter/fieldoperation.png)

The dashboard for the Field operation Component (see Image 1) provides the tabular view for the list of the available machinery.  The vehicle selection filter has an option to select the vehicle ID.  The simplistic interface shows all the necessary data directly, indicating driver behavior as an output of classification based on the requirements given in the pilot 5.1.

### Dependencies (either internal to DEMETER or bound to the pilot)

- fleetNET platform -fleet monitoring platform for tracking of vehicles GPS location, and collection of various statistics for the vehicle over the CAN interface 
- FEDE Mac
hinery control exercised by Fede Specialty Crops Platform (SCP) that links via GPRS to the tractors and sprayers in the field.

AIM models and DEH are used.
