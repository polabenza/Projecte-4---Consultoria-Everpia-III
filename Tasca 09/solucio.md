## TASCA 09 Servidor fitxers Linux. NFS

**Per començar aquesta pràctica crearem 2 màquines virtuals de Linux, una amb Ubuntu i l'altre amb Zorin**

**Per començcar crearem dos grups**

```
sudo groupadd devs && sudo groupadd admins
```

![image](./img/2.png)

![image](./img/3.png)


**El següent pas serà crear els usuaris i afegir-los al grup corresponent**

```
sudo useradd -m -s /bin/bash -G devs dev01
```

```
sudo useradd -m -s /bin/bash -G admins admin01
```

![image](./img/4.png)

![image](./img/5.png)

**Ara crearem els directoris per als projectes de desenvolupament i les eines d'administració**

```
sudo mkdir -pv /srv/nfs/dev_projects
```

![image](./img/6.png)

```
sudo mkdir -pv /srv/nfs/admin_tools
```

![image](./img/7.png)


**Aqui podem veure els permisos de cada grup i a que poden accedir**

![image](./img/9.png)






