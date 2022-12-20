### Description
This component presents the animal feeding quality based on food and water consumption and comparison with technology required consumption.  The component provides the UI dashboard with food level in the silo with estimated consumption. The animal feeding consumption can be then assessed by farmers based on the level of the food in the silo. The components receive data as an input in the  DEMETER  AIM format.  More specifically, data about silo volume, flock age, animal species, food type, food density and the silo empty threshold value. These data are then analyzed, and the output of the classification process is then provided to the dashboard output. The component is generic and can be used not only for poultry but it can be employed in any use cases, where it is necessary to monitor the feeding of the animals.


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

[Image 1 – Knowage dashboard for Poultry feeding component](https://sasagronet.blob.core.windows.net/demeter/poultryfeeding.png)


The dashboard for the  Poultry feeding  Component  (see Image 1)  provides the graphical view for the animal feeding quality, food type and food silo level. The simplistic interface shows all necessary data directly,  indicating the animal feeding quality and level of the food in the silo as an output of classification based on the requirements given in pilot 4.4.

### Dependencies 
(either internal to DEMETER or bound to the pilot)

- poultryNET platform - provides easy-to-use decision support instructions based on the real-time observations of the parameters of interest and digitized domain expertise enabling farmers to manage all steps in the poultry production. The platform has embedded algorithms and its own dashboard and analytics.


AIM models and DEH are used.

