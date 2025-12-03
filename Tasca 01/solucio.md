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


