### Description
This component for transport condition covers the post-farm cycle for poultry production providing insight into environmental conditions during the transport to different stakeholders.  The components receive data (latitude, longitude, CO2, temperature and humidity) as an input in the DEMETER AIM format.  After analysis, the output of the classification process is provided to the dashboard.
Deployment details



### Deployment details 

To start API first login to container registry:
```
sudo docker login demeter.azurecr.io
user: demeter
pass: dHVlOXWfZ/Ep2x1aj24pyI5jqqggjLR9

```
Start API container:
```
sudo docker-compose pull
sudo docker-compose up -d
```

check API at:
http://localhost:8001/swagger/index.html

### Screenshots  

[Image 1 – Knowage dashboard for Transport conditions component](https://sasagronet.blob.core.windows.net/demeter/trasportcond.png)

The dashboard for the Poultry well-being Component (see Image 1) provides a graphical view of the animal transport condition based on specific environmental parameters.  The simplistic interface shows all the necessary data, indicating the animal transport during the exchange of goods between actors in the supply chain.  The main output is a classification of transport conditions based on the requirements given in pilot 4.4. 

### Dependencies 
(either internal to DEMETER or bound to the pilot)

- fleetNET platform -fleet monitoring platform for tracking of vehicles GPS location, and collection of various statistics for the vehicle over the CAN interface

- agroNET platform -agriculture platform providing holistic overview of monitored fields, installed devices (weather stations for monitoring air temperature, air humidity, precipitation, leaf wetness, wind speed and direction, radiation; devices equipped with sensors for monitoring soil conditions, ; smart pheromone traps with cameras embedded to monitor insects population, and expert modules providing instructions to farmers based on gathered infield measurements.

AIM models and DEH are used.



