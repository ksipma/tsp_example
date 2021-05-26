### TSP-probleem scalen voor grote toepassingen

### benodigd voor doen van deze workshop
- Docker(https://docs.docker.com/get-docker/)
- Jupyter notebook(anacondas: https://www.anaconda.com/products/individual)

### installs
Deze packages zijn benodigd voor vanmorgen
```
pip install prefect
pip install requests
pip install pandas
pip install numpy
pip install python-tsp
```

### docker command for osrm

Plak dit commando voor het starten van de osrm-engine. Deze engine maakt het mogelijk om afstanden/tijden van routes te berekenen, in dit geval voor Overijssel.
```
docker run -d -p 5000:5000 -e OSRM_PBF_URL='https://download.geofabrik.de/europe/netherlands/overijssel-latest.osm.pbf' --name osrm-backend peterevans/osrm-backend:latest
```


### docker command voor starten omgeving
```
prefect backend server
prefect server start
```
En dan in een nieuwe shell:
```
prefect agent local start
```

