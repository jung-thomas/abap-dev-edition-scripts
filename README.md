# ABAP Developer Edition Useful commands and scripts


## License
This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.

## Administration
- Hostname: vhcala4hci
- Default Password: Ldtf5432

### Shell
```shell
docker exec -it a4h /bin/bash
```

### ABAP Stop
```shell
su - a4hadm
/usr/sap/hostctrl/exe/sapcontrol -nr 0 -function StopSystem
```

### ABAP Status
```shell
su - a4hadm
dpmon 0
```

### HANA Stop
```shell
su - hdbadm
./HDB stop
```

### HANA Status
```shell
su - hdbadm
./HDB info
```

### Docker Run
```shell
docker run --stop-timeout 3600 -i --name a4h -h vhcala4hci -p 3200:3200 -p 3300:3300 -p 8443:8443 -p 30213:30213 -p 30215:30215 -p 50000:50000 -p 50001:50001 -p 50013:50013 -p 50014:50014 store/saplabs/abaptrial:1909 -skip-limits-check -agree-to-sap-license
```

