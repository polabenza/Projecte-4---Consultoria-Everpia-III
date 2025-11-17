# 📂 Introducció

Molt bé, equip de consultors júniors,  

En el nostre projecte ens trobem amb un requisit tècnic molt habitual per part dels nostres clients: **la centralització de dades en entorns Linux** 🐧.

---

## 🏢 El Cas Client: DevOptimize Solutions

- **Client:** DevOptimize Solutions  
- **Sector:** Startup de desenvolupament de programari  
- **Sistema operatiu:** Linux exclusivament  

### Problema crític

- El codi font i els actius (documents de disseny, scripts) estan **descontrolats**  
- Cada desenvolupador té **còpies locals**  
- Resultat: **errors de versió constants** i **pèrdua d'eficiència** ⚠️

---

## 💡 Solució proposada

Implementar un **servidor de fitxers centralitzat** utilitzant **NFS (Network File System)**:

- Entorn 100% Linux → **NFS natiu** és la solució més ràpida i eficient  
- Sense entorn d’autenticació centralitzada (segons requisits del client)  
- Mostrar limitacions de la solució actual  

---

## 🖥️ Tasca pràctica

Crear una demostració del sistema amb:

1. **Servidor NFS (NFSv3)**  
2. **Client Linux** que consumeixi els recursos compartits  

### Accions a realitzar:

- Crear **usuaris i grups** per simular l’entorn del client 👥  
- Demostrar **control d’accés** mitjançant:
  - Opcions d’exportació a `/etc/exports` 📄  
  - Permisos del sistema de fitxers (`chmod`, `chown`) 🔑  

L’objectiu és que el client pugui veure **com quedarà la solució proposada** i entendre les seves limitacions actuals.

