**GUIA TASCA 05**

**Primer de tot instal·lem SSH**

```
sudo apt install ssh
```

![image](./img/1.png)

**Comprovem quina adreça té el server**

```
ip addr show
```

![image](./img/2.png)

**Comprovem la connexió, desde Powershell**

```
ssh polabenza@192.168.56.102
```

***podem veure com tenim connexió desde windows com si estuguessim a Linux***

![image](./img/3.png)


**Un cop que ja estem dins de la maquina el seguent pas que farem sera modificar l'arxiu de configuració, per poder editar-lo primer escriurem la seguent comanda**

```
sudo nano /etc/ssh/sshd_config
```

**Canviarem les següents lineas:**

![image](./img/4.png)


**Comprovem que només es pot iniciar sessió en root localment i no per SSH.**

```
sudo passwd root
```

![image](./img/5.png)


**Si fem SSH com a root, no ens deixara**

![image](./img/6.png)


**Però podem iniciar sessió de manera local sense problemes**

![image](./img/7.png)



**Per donar connexió remota només a usuaris autoritzats crearem ara un nou usuari**

```
sudo useradd -m -s /bin/bash usuari2
```

![image](./img/8.png)

**Li posem una contrasenya a usuari2**

```
sudo passwd usuari2
```


**Afegim usuari autoritzat al arxiu SSH agefint la següent linia**

```
AllowUsers usuari
```

![image](./img/9.png)


**Reiniciem el servei per aplicar els canvis**

```
sudo systemctl restart ssh
```

**Ara amb usuari si funciona pero amb usuari2 no**

![image](./img/11.png)

![image](./img/10.png)

