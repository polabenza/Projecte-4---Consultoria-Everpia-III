# T01  
## DRP: Còpies de Seguretat

---

### **1. Què copiar? (Priorització)**  
Jo crec que el més important seria:  
- La **base de dades**, ja que canvia constantment.  
- Els **documents de projectes**.  
- Les **carpetes personals dels usuaris**, perquè és feina del dia a dia.

No crec que sigui necessari fer còpia dels 10 equips clients. Només cal guardar el que els tècnics deixen temporalment a *Documents*. El que faria seria que aquestes carpetes es guardin automàticament al servidor i així no cal fer còpies dels ordinadors.

---

### **2. Periodicitat i Tipus de Còpia**  
Per a les **bases de dades** (les més crítiques):  
- Cada **4 hores** incremental, cada **nit** completa i cada **diumenge** completa

Per als **documents de projectes** i **carpetes personals** faria 1 incremental diària, 1 completa setmanal i 1 completa mensual. 

---

### **3. Mitjans i Ubicació**  
Utilitzaria:  
- **NAS local** perquè permet còpies ràpides.  
- **Còpia al núvol** per tenir dades fora de l’empresa.  
- **1 disc dur extern** opcionalment per tenir una còpia offline.

**Regla 3-2-1:**  
- **3 còpies:** original + NAS + Cloud  
- **2 tipus de suports:** NAS i Cloud  
- **1 còpia fora de lloc:** al Cloud


# Fase 2 (en parelles)– Proposta Unificada (Curt) 

Després de comparar les respostes individuals, hem dit de fer un esquema de còpies **3-2-1** basat en centralitzar totes les dades al servidor (BD, projectes i carpetes personals), així no haurem de fer còpies dels 10 equips.  
Utilitzarem un **NAS local** per a còpies ràpides i el **Cloud** com a còpia fora de lloc.  
La BD tindrà còpies molt freqüents i els documents una periodicitat normal.

## Taula de Proposta Unificada

| **Element** | **Proposta de la Parella** | **Justificació** |
|-------------|-----------------------------|------------------|
| **Dades Crítiques** | BD, documents de projectes, carpetes personals al servidor | Són les dades essencials. Centralitzar-ho evita copiar els 10 PCs. |
| **Periodicitat (BD)** | Incremental cada 4h, completa cada nit i setmanal | La BD canvia sovint i necessita seguretat alta. |
| **Tipus de Còpia (BD)** | Incrementals + completes | Incrementals ràpides, completes per restauració estable. |
| **Periodicitat (Docs/Usuaris)** | Incremental diària, completa setmanal i mensual | No canvien tan sovint com la BD. |
| **Mitjà 1 (Local)** | NAS | Ràpid i ideal per restauracions immediates. |
| **Mitjà 2 (Extern)** | Cloud | Còpia fora de lloc segons la regla 3-2-1. |


# Fase 3: Treball en grup

## 1. Debat i Selecció
Cada parella presenta el seu esquema.  
El grup debat els pros i contres de cada proposta (**cost**, **temps de recuperació**, **seguretat**, **simplicitat**).

## 2. Disseny de la Política Final
El grup ha de redactar la **Política de Còpies de Seguretat Definitiva** que presentaran a l'empresa *"Muntatges i Serveis Tècnics SL"*.

---

## 1 Dades Objecte de Còpia

| Tipus                             | Objecte de Còpia                                | Criticitat | Comentari                                   |
|----------------------------------|--------------------------------------------------|------------|----------------------------------------------|
| Servidor de Fitxers (Ubuntu)     | Bases de Dades (Comptabilitat i Clients)         | Alta       | Canvi constant, RPO 4h, RTO 4h               |
|                                  | Documents de Projectes                           | Mitjana    | Gran volum, canvis moderats                 |
|                                  | Carpetes Personals dels Usuaris                 | Mitjana    | Canvis diaris                               |
| Equips Clients (Windows 10/11)   | Carpeta Documents                                | Mitjana    | Alguns informes i arxius temporals          |

---

## 2 Cronograma Setmanal Detallat

| Dia       | Dades                   | Tipus de Còpia                        | Mitjà                  |
|-----------|-------------------------|----------------------------------------|------------------------|
| Dilluns   | Bases de Dades          | Incremental cada 4h                    | NAS                    |
|           | Documents de Projectes  | Incremental diari                      | NAS                    |
|           | Carpetes Personals      | Incremental diari                      | NAS                    |
|           | Clients Windows         | Incremental diari                      | NAS                    |
| Dimarts   | *Idèntic a Dilluns*     |                                        |                        |
| Dimecres  | *Idèntic a Dilluns*     |                                        |                        |
| Dijous    | *Idèntic a Dilluns*     |                                        |                        |
| Divendres | Bases de Dades          | Diferencial diària + Completa setmanal | NAS + Disc dur extern  |
|           | Documents de Projectes  | Completa setmanal                      | Disc dur extern        |
|           | Carpetes Personals      | Completa setmanal                      | Disc dur extern        |
|           | Clients Windows         | Incremental diari                      | NAS                    |
| Dissabte  | *Idèntic a Dilluns*     |                                        |                        |
| Diumenge  | Bases de Dades          | Completa mensual                        | Cloud (AWS)            |
|           | Documents de Projectes  | Completa mensual                        | Cloud (AWS)            |
|           | Carpetes Personals      | Completa mensual                        | Cloud (AWS)            |

---

## 3 Elecció de Mitjans i Ubicació (Regla 3-2-1)

| Categoria            | Mitjà                    | Ubicació                           | Responsabilitat                   |
|----------------------|---------------------------|------------------------------------|----------------------------------|
| Mitjà 1 (Local)      | NAS intern                | Sala de Servidors, accés restringit | Administrador TI                 |
| Mitjà 2 (Extern)     | Disc dur extern (setmanal)| Armaris segurs a l’empresa         | Administrador TI                 |
| Ubicació Fora de Lloc| Cloud (AWS)               | Servei Cloud, dades xifrades        | Administrador TI i seguretat     |

**Compliment de la regla 3-2-1:**
- **3 còpies**: NAS, disc extern, cloud  
- **2 mitjans diferents**: NAS + disc extern/cloud  
- **1 ubicació fora de lloc**: Cloud  

---

## 4 Estratègia de Recuperació (RTO/RPO)

### Bases de Dades (Comptabilitat/Clients)
- **RPO 4 h**: Còpies incrementals cada 4 hores per minimitzar pèrdua de dades.  
- **RTO 4 h**: Restauració prioritària des del NAS o, si cal, des del disc dur extern.  
  El cloud actua com a última via en cas de desastre major.

### Documents de Projectes / Carpetes Personals / Clients Windows
- **RPO 24 h**: Còpies incrementals diàries asseguren que només es perd un dia de treball.  
- **RTO ≤ 24 h**: Restauració ràpida des del NAS per incidents menors.

---

## Procediment en cas de fallada
1. Restaurar **dades crítiques (BD)** des del NAS.  
2. Si el NAS no està disponible, utilitzar el **disc extern**.  
3. En cas de desastre total, recuperar la **còpia mensual al Cloud**.
