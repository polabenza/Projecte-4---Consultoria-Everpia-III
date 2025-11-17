# 📚 Introducció
La primera hora el vostre responsable de seguretat us presenta el tema de les còpies de seguretat a partir d’un material didàctic.  
A continuació, caldrà que hi treballeu els aspectes del tema i ho fareu mitjançant una **dinàmica cooperativa**.

---

# 🏢 Presentació del cas client
**"Muntatges i Serveis Tècnics SL"** és una petita empresa dedicada a la instal·lació i manteniment d'equips industrials.

## 💻 Infraestructura Tècnica
- **Servidor de Fitxers (Ubuntu Server):** Conté tota la documentació crítica:
  - 📄 **Documents de Projectes:** Plànols, especificacions tècniques (300 GB, creixement moderat)
  - 🗃️ **Bases de Dades (Comptabilitat i Clients):** Crítiques i d'ús diari (20 GB, canvi constant)
  - 👤 **Carpetes Personals dels Usuaris:** Per a la feina diària (100 GB)
- **10 Equips Clients (Windows 10/11):** Els usuaris treballen majoritàriament amb fitxers del servidor, però alguns tècnics guarden temporalment informes i altres arxius importants a la carpeta **Documents**.
- **Connexió a Internet:** Fibra òptica de 600 Mbps (simètrica) 🌐

## ⏱️ Requisits de Recuperació
- **Temps de Recuperació (RTO):** Les dades de Comptabilitat/Clients han d'estar disponibles en menys de **4 hores** ⏳
- **Pèrdua de Dades Admesa (RPO):** 
  - Majoria de dades: fins a **24 hores** de pèrdua màxima
  - Comptabilitat/Clients: **no més de 4 hores** de treball perdut ⚠️
- **Retenció:** Cal guardar les dades amb un historial d'almenys **un mes** 🗓️

