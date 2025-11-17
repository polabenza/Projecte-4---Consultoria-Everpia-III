# 📘 Introducció al cas
A la tasca anterior heu dissenyat una **política de còpies de seguretat** pel nostre nou client **"Muntatges i Serveis Tècnics SL"**.  
Ara toca **passar a l’acció** i portar a la pràctica l’estudi anterior.  

El client demana que s’elaborin unes **guies tècniques amb proves de concepte** perquè el seu personal estigui qualificat per implantar el pla de còpies de seguretat.

---

# 🖥️ Part 1: Còpia de seguretat dels equips clients Windows
Encara que en principi el DPR no contemplaria fer còpia dels arxius locals dels equips clients, **es farà una excepció** amb l’equip Windows del director de l’empresa.  

Aquest equip conté informació important que **no es vol tenir accessible al servidor de fitxers**.  

## 📂 Política de còpia 3-2-1
- 🔹 Còpia al **disc secundari** de l’equip  
- 🔹 Còpia al **cloud** amb Google Drive via **Duplicati**  

## 🖥️ Prova de concepte
1. Crear una **màquina virtual Windows 11** amb dos discs:
   - Disc principal: sistema operatiu  
   - Disc secundari: 10 GB per còpies de seguretat  
2. Simular Google Drive amb un **compte específic** (no escolar).  
3. Configurar còpies:
   - Perfil de l’usuari cada **hora** al disc secundari  
   - A les **18:00** a Google Drive  

## 📝 Procediment
- Documentar instal·lació de **Duplicati**  
- Configurar plans de còpia i observar funcionament  
- Afegir arxius a **Documents**  
- Esborrar contingut de Documents i restaurar des del **disc secundari**  
- Comprovar restauració des del **cloud**

---

# 🐧 Part 2: Còpia de seguretat del servidor Linux
Per fer les còpies del servidor Linux, la solució proposada és **Duplicity**, combinat amb **cron** per implementar polítiques de còpia automàtiques.

## 🖥️ Prova de concepte
1. Crear una **màquina virtual Ubuntu Server** amb un segon disc de 10 GB que simularà una unitat auxiliar.  
2. Inicialitzar i formatejar en **XFS**, muntar manualment a `/media/backup` (crear carpeta primer).  
3. Instal·lar **Duplicity**.  
4. Crear 2 usuaris addicionals amb carpeta personal. Crear 4 arxius de **10 MB** a `/home`.  
5. Fer còpia de seguretat de `/home`.  
6. Esborrar arxius i restaurar per comprovar recuperació.  
7. Afegir un arxiu de **4 MB** i fer nova còpia (**incremental**).  
8. Desmuntar unitat de backup.

## ⚙️ Automatització amb scripts i cron
**Nota de seguretat:** La unitat de backup ha d’estar **desmuntada per defecte**. Sempre muntar abans i desmuntar després.

1. Crear script `fullbackup.sh`:
   - Còpia completa de `/home` al volum muntat  
   - Usar variable d’entorn `PASSPHRASE` per no escriure la passphrase manualment  
   - Donar permisos d’execució  
2. Programar cron (root) per executar **diumenges a les 23:00**  
3. Crear script `incrementalbackup.sh`:
   - Còpies **incrementals** de `/home`  
   - Assignar `PASSPHRASE` i permisos d’execució  
4. Programar cron (root) per executar **dilluns a dissabte a les 23:00**

