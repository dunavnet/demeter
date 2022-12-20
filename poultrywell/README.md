### Description

This component for poultry well-being provides the overall poultry stress based on parameters from the environment and patterns detected from the environment and video/ microphone. The component provides the   UI dashboard with the following data: air temperature, air humidity, airflow, light intensity, CO2 level, power loss, animal species, detected stress level, flock age, safety instruction. The components receive data as an input in the DEMETER AIM format. These data are then analyzed, and the output of the classification process is provided to the dashboard output. The animal well-being quality can be then directly monitored by farmers altogether with a set of parameters captured from the environment.

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

[Image 1 – Knowage dashboard for Poultry well-being component](https://sasagronet.blob.core.windows.net/demeter/poultrywellbeing.png)

The dashboard for the Poultry well-being Component (see Image 1) provides the graphical view for the animal well-being based on environmental parameters.  The simplistic interface shows all necessary data directly, indicating the animal well-being as an output of classification based on the requirements given in the pilot 4.4.

### Dependencies 
(either internal to DEMETER or bound to the pilot)

- poultryNET platform - provides easy-to-use decision support instructions based on the real-time observations of the parameters of interest and digitized domain expertise enabling farmers to manage all steps in the poultry production. The platform has embedded algorithms and its own dashboard and analytics 

AIM models and DEH are used.

