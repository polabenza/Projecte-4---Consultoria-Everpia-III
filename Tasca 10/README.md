# 🖨️ Introducció

Molt bé, equip.  

A la nostra consultora, **EverPia**, busquem constantment **optimitzar els recursos dels nostres clients** per reduir costos i simplificar la gestió.  

Un dels punts més caòtics en qualsevol oficina és la **gestió d'impressores**:  
- Drivers incompatibles ⚠️  
- Costos de tòner descontrolats 💸  
- Equips que no saben a quina impressora enviar la feina 🖨️

La solució professional: **Servidor d'Impressió Centralitzat**.

---

## 🏢 Cas Client: DevOptimize Solutions

- Requisit: Centralitzar la impressió en tots els departaments  
- Clients Linux: Zorin OS 🐧  
- Servidors: Ubuntu Server 🖥️  

---

## 🎯 La Vostra Missió: Prova de Concepte (PoC)

Abans de comprar impressores de xarxa cares, el client vol veure una **PoC** que demostri que un **servidor Linux pot gestionar una impressora** i compartir-la amb els clients Zorin.  

### 💡 Solució de simulació

- Utilitzarem la **impressora virtual `cups-pdf`**  
- Com funciona: imprimeix documents en fitxers PDF al servidor, en lloc de paper 📄➡️💾  

Objectiu: **configurar l’escenari i demostrar que un client pot enviar treballs d’impressió al servidor**.

---

## 🖥️ Escenari de Treball

- **Màquina 1 (Servidor):** Ubuntu Server  
  - Interfície NAT + interfície Host-Only  
- **Màquina 2 (Client):** Zorin OS (Desktop)  
  - Mateixa configuració de xarxa que el servidor  

---

## 📝 Pasos PoC (Prova de Concepte)

1. Instal·lació de **CUPS** al servidor  
2. Instal·lar **impressora virtual (`cups-pdf`)**  
3. Configurar l’administració de CUPS i permetre que **CUPS escolti per totes les interfícies** 🌐  
4. Compartir la impressora mitjançant **el frontal web de CUPS**  
5. Afegir la impressora al **client Zorin**  
6. Fer una **prova d’impressió de diversos documents** 📝  
7. Comprovar al servidor que **s’han generat els fitxers PDF corresponents**  

---

## 📸 Documentació

- Registrar totes les **comandes utilitzades**  
- Incorporar **captures de pantalla** per demostrar el correcte funcionament de la prova ✅

