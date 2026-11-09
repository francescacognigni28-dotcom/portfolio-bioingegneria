# Sviluppo di un Modello Numerico agli Elementi Finiti (FEM) per il Confronto di Stent in CoCr L605 e PLA per il Trattamento dell'Aterosclerosi

**Corso:** *Meccanica Computazionale per la Clinica e la Chirurgia* (Voto: **30/30**)  
**Università degli Studi di Padova** – Corso di Laurea Magistrale in Bioingegneria (A.A. 2025/2026)  
📄 **[Visualizza l'Elaborato Tecnico Completo (PDF)](./Elaborato_MeccanicaComputazionale_Stent_Auxetici_FEM.pdf)**

---

## Obiettivo del Progetto

Analizzare mediante simulazione strutturale agli elementi finiti (**FEM**) la progettazione e la meccanica di *deployment* di uno **stent coronarico auxetico ibrido di tipo *re-entrant* (RE)** espandibile con palloncino, valutando l'influenza del materiale a parità di geometria attraverso il confronto tra:
1. **Lega metallica Cobalto-Cromo (CoCr L605)**, standard clinico per gli stent permanenti;
2. **Acido Polilattico (PLA)**, biopolimero bioriassorbibile.

---

## Metodologia e Strumenti Software

### 1. Modellazione Geometrica CAD 3D e Reverse Engineering
* **Rhino 8:** Modellazione 2D della griglia auxetica *re-entrant* e avvolgimento cilindrico 3D per formare lo stent tubolare (circonferenza base $6,85\text{ mm}$, lunghezza $9\text{ mm}$, spessore $0,04\text{ mm}$, altezza singola maglia $0,9\text{ mm}$).
* **Geomagic Design X:** Rifinitura superficiale dello stent tramite cilindri concentrici per garantire il riconoscimento esatto delle superfici in Abaqus; isolamento e ricostruzione dal *Vascular Model Repository* (`.stl` $\rightarrow$ `.step`) di un segmento di **arteria coronaria discendente anteriore sinistra (LAD)** di lunghezza $3\text{ mm}$, diametro esterno medio $3,63\text{ mm}$, diametro interno medio $2,72\text{ mm}$ e spessore di parete $0,46\text{ mm}$.

### 2. Modelli Costitutivi dei Materiali (Abaqus CAE)
* **CoCr L605 (Elasto-Plastico Isotropo):** $\rho = 8800\text{ kg/m}^3$, $E \approx 200\text{ GPa}$, $\nu = 0,3$, snervamento $\sigma_y = 519,62\text{ MPa}$ ($\varepsilon = 0,003$), rottura $\sigma_r = 1141,52\text{ MPa}$ ($\varepsilon = 0,50$).
* **PLA (Elasto-Plastico Isotropo):** $\rho = 1250\text{ kg/m}^3$, $E = 3000\text{ MPa}$, $\nu = 0,36$, snervamento $\sigma_y = 30\text{ MPa}$, rottura $\sigma_r = 45\text{ MPa}$ ($\varepsilon_p = 6\%$).
* **Arteria Coronaria LAD (Iperelastico di Ogden del 3° Ordine):** $\rho = 1070\text{ kg/m}^3$, comportamento quasi-incomprimibile ($\nu = 0,49$, formulazione ibrida).

### 3. Simulazione Non Lineare Multi-Step e Discretizzazione Mesh
Simulazione statica non lineare (`Nlgeom = ON`, *Automatic Stabilization* con frazione di energia dissipata $2 \cdot 10^{-4}$) articolata nelle **4 fasi cliniche di impianto**:
1. **Crimping:** Compressione radiale dello stent ($U_1 = -0,18\text{ mm}$, riduzione diametrale del $9\%$) tramite cilindro di crimpaggio shell.
2. **Crimping Retraction:** Rimozione parziale del vincolo radiale per valutare il ritorno elastico post-crimpaggio (*crimp recoil*).
3. **Espansione:** Dilatazione radiale tramite palloncino fino al contatto e al sostegno meccanico della parete arteriosa LAD ($U_1 = +0,55\text{ mm}$).
4. **Expansion Retraction:** Scarico del palloncino per determinare il ritorno elastico finale (*stent recoil*) e lo stato tensionale residuo sul vaso.

* **Mesh:** Elementi tetraedrici lineari `C3D4` per lo stent (*seed* $0,05\text{ mm}$), elementi tetraedrici ibridi `C3D4H` con infittimento locale (*seed* $0,15\text{ mm}$) nella zona di contatto per la LAD, ed elementi shell `S4R` con meshatura strutturata *sweep* per cilindro e palloncino.

---

## Principali Risultati Quantitativi

| Parametro Funzionale / Meccanico | Stent in CoCr L605 | Stent in PLA |
| :--- | :---: | :---: |
| **Diametro post-crimping ($D_{\text{crimp}}$)** | $2,10\text{ mm}$ | $2,10\text{ mm}$ |
| **Crimp Recoil ($CR$)** | **$3,33\%$** | **$5,24\%$** |
| **Diametro di picco espansione ($D_{\text{exp}}$)** | $2,61\text{ mm}$ | $2,60\text{ mm}$ |
| **Expansion Recoil ($ER$)** | **$3,45\%$** | **$5,77\%$** |
| **Foreshortening** | **$-9,57\%$** | **$-9,57\%$** |
| **Coefficiente di Poisson equivalente ($\nu_{\text{eq}}$)** | **$-2,53$** | **$-2,48$** |
| **Tensione di Von Mises max su stent (Espansione)** | $\sim 916\text{ MPa}$ | $\sim 45\text{ MPa}$ |
| **Deformazione plastica equivalente max (`PEEQ`)** | $0,387$ | $0,248$ |
| **Tensione di Von Mises sulla LAD (Picco $\rightarrow$ Post-recoil)** | $75,9\text{ kPa} \rightarrow 41,9\text{ kPa}$ | $78,4\text{ kPa} \rightarrow 40,5\text{ kPa}$ |
