# Instalación de grafana

**Paso 1--> Dependencias de Grafana** :

 
 - sudo apt install -y apt-transport-https
 - sudo apt install -y software-properties-common wget


**Paso 2 --> Repositorio de Grafana**
- wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -

- sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"

- sudo apt update

**Paso 3 --> Instalar Grafana**
- sudo apt install grafana

**Paso 4 --> Ininiar Grafana**
- sudo systemctl daemon-reload

- sudo systemctl enable grafana-server

- sudo systemctl start grafana-server

- sudo systemctl status grafana-server