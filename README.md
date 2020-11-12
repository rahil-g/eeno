# GPF: Green Power Forwarding

## PART I: Real-time network power monitoring

OS: Ubuntu 16.04.07 LTS

Required packages:
Python3, 
Pip3
```
$ sudo apt-get update; sudo apt-get install python3-pip -y; sudo -H pip3 install --upgrade pip
```

First, install all packages from the packages.txt file -
```
sudo apt-get update ; cat packages.txt | xargs sudo apt-get install -y
```

Next, install the required Python libraries from the requirements.txt file -
```
sudo -H pip3 install -r requirements.txt
```

Start the SNMP agents simulation using the sim_snmp.py app -
```
python3 sim_snmp.py 3
```

On another terminal, start the Energy Monitoring System app -
```
python3 EMS.py
```

On another terminal, start the REST endpoints app -
```
python3 REST_endpoint.py
```
