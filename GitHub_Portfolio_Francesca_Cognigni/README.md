# Portfolio Ingegneristico – Francesca Cognigni

**Ingegnere Biomedico (L-8/L-9) | Laureanda Magistrale in Bioingegneria Industriale (LM-21)**  
*Università degli Studi di Padova*

![Abaqus CAE](https://img.shields.io/badge/FEM-Abaqus_CAE-17365D?style=flat-square)
![Rhino 8](https://img.shields.io/badge/CAD_3D-Rhino_8_%7C_Fusion_360-2B6CB0?style=flat-square)
![Geomagic Design X](https://img.shields.io/badge/Reverse_Engineering-Geomagic_Design_X-2B6CB0?style=flat-square)
![MATLAB](https://img.shields.io/badge/Computing-MATLAB_%7C_Python_%7C_SQL-17365D?style=flat-square)
![Medical Imaging](https://img.shields.io/badge/Bioimaging-3D_Slicer_%7C_DICOM_%7C_TIFF-2B6CB0?style=flat-square)
![Biomaterials](https://img.shields.io/badge/R%26D-Biomateriali_%26_Biofabbricazione-17365D?style=flat-square)

---

## Presentazione

Benvenuti nel mio repository di portfolio tecnico-scientifico. Questa raccolta documenta i principali progetti di **simulazione computazionale agli elementi finiti (FEM)**, **modellazione CAD 3D e reverse engineering anatomico**, **elaborazione di bioimmagini cliniche** e **caratterizzazione meccanica e biologica di biomateriali e scaffold per medicina rigenerativa** svolti durante il percorso di Laurea Triennale in Ingegneria Biomedica e di Laurea Magistrale in Bioingegneria Industriale presso l'**Università degli Studi di Padova** (media ponderata **27,3/30**, esami terminati).

> **Disponibilità Professionale:** Disponibile per **tirocini formativi extracurriculari** e **posizioni junior / entry-level** negli ambiti *R&D Dispositivi Medici, Calcolo Strutturale e Simulazione FEM, Progettazione CAD 3D, Caratterizzazione Biomateriali & Testing Meccanico, Elaborazione Bioimmagini, Qualità & Affari Regolatori*.

---

## Indice dei Progetti e Lavori di Tesi

| # | Progetto / Tesi | Ambito Tecnico | Strumenti, Normative e Metodologie | Documentazione |
| :-: | :--- | :--- | :--- | :--- |
| **01** | **[Simulazione FEM del Deployment di Stent Coronarici Auxetici in CoCr L605 e PLA](./01_FEM_Stent_Coronarici_Auxetici_CoCr_PLA/)** | Meccanica Computazionale & Dispositivi Vascolari | `Abaqus CAE`, `Rhino 8`, `Geomagic Design X`, Modello iperelastico di Ogden (3° ordine), Elasto-plasticità, Analisi non lineare (`Nlgeom`) | [Elaborato PDF](./01_FEM_Stent_Coronarici_Auxetici_CoCr_PLA/Elaborato_MeccanicaComputazionale_Stent_Auxetici_FEM.pdf) |
| **02** | **[Scaffold 3D Bioceramici in β-TCP per la Rigenerazione Ossea](./02_Scaffold_3D_Bioceramici_Rigenerazione_Ossea/)** | Struttura e Meccanica dei Biomateriali | Stampa 3D a estrusione coassiale (CSH), `DLP` (`TPMS Gyroid`), Doping ionico ($\text{Cu}^{2+}$, $\text{Sr}^{2+}$), Prove a compressione `ISO 13314`, Degradazione *in vitro* (SBF, Tris-HCl) | [Presentazione PDF](./02_Scaffold_3D_Bioceramici_Rigenerazione_Ossea/Presentazione_Scaffold_Bioceramici_BetaTCP.pdf) |
| **03** | **[Biofabbricazione Cardiaca: Controllo Strutturale e Allineamento Tissutale in Modelli Ventricolari](./03_Biofabbricazione_Cardiaca_Modelli_Ventricolari/)** | Biofabbricazione & Tissue Engineering | Bioprinting 3D *free-standing* (`FIG` – *Fibre-Infused Gel*), Metodo `FRESH` (collagene nativo), Filatura `FRJS` (*Focused Rotary Jet Spinning*), Analisi elettrofisiologica e `PIV` | [Presentazione PDF](./03_Biofabbricazione_Cardiaca_Modelli_Ventricolari/Presentazione_Biofabbricazione_Del_Cuore.pdf) |
| **04** | **[Caratterizzazione e Biocompatibilità di Compositi Polimerici Rinforzati con Fibre di Carbonio (CFRP)](./04_Biocompatibilita_Compositi_CFRP_Dispositivi_Impiantabili/)** | Biomateriali Avanzati & Dispositivi Impiantabili | `CF-SMC`, Stampa 3D `FFF`, Spettroscopia e Microscopia (`FTIR`, `EDX`, `SEM`, `AFM`), Biocompatibilità *in vitro* (`Test di Ames`, saggio `MTT`) e *in vivo* | [Presentazione PDF](./04_Biocompatibilita_Compositi_CFRP_Dispositivi_Impiantabili/Presentazione_Compositi_CFRP_Dispositivi_Impiantabili.pdf) |
| **05** | **[Tesi Triennale: Il Sistema Pancreas Artificiale e la sua Validazione In Silico](./05_Tesi_Triennale_Pancreas_Artificiale_In_Silico/)** | Modellazione Fisiologica & Controllo Automatico | Modelli compartimentali glucosio-insulina, Sensori `CGM`, Microinfusori, Algoritmi *closed-loop*, `UVA/Padova T1D Simulator` | [Tesi PDF](./05_Tesi_Triennale_Pancreas_Artificiale_In_Silico/Tesi_Triennale_Pancreas_Artificiale_Validazione_In_Silico.pdf) |

---

## Competenze Tecniche Principali

* **Modellazione CAD 3D, Analisi FEM & Reverse Engineering:**
  * **Abaqus CAE:** Simulazioni strutturali statiche non lineari (`Nlgeom`), contatti *Surface-to-Surface* con formulazione *Penalty*, vincoli cinematici `MPC Beam` in sistemi di coordinate cilindriche, calibrazione di modelli costitutivi elasto-plastici isotropi e iperelastici incomprimibili (Ogden di 3° ordine), discretizzazione con elementi `C3D4`, `C3D4H` (formulazione ibrida) e shell `S4R`.
  * **Rhino 8 & Autodesk Fusion 360:** Modellazione CAD 3D di dispositivi vascolari (stent coronarici auxetici *re-entrant*) e componenti biomedicali.
  * **Geomagic Design X:** *Reverse engineering* di geometrie anatomiche vascolari da repository clinici, isolamento di segmenti arteriosi e rifinitura superficiale di mesh `.stl` e solidi `.step`.
* **Programmazione Scientifica & Bioimmagini:**
  * **MATLAB & Simulink:** Calcolo numerico, simulazione *in silico* di modelli fisiologici compartimentali e sistemi di controllo *closed-loop* (`UVA/Padova Type 1 Diabetes Simulator`), elaborazione di bioimmagini (`DICOM`, `TIFF`), analisi di segnali biomedici e analisi statistica.
  * **Python, SQL, 3D Slicer:** Elaborazione dati, interrogazione di database relazionali e segmentazione tridimensionale di immagini mediche.
* **Biomateriali, Biofabbricazione & Testing:**
  * Studio di processi di **Stampa 3D a estrusione/coassiale**, **DLP**, **FFF**, biostampa **FRESH** e filatura **FRJS**; caratterizzazione di bioceramici ($\beta\text{-TCP}$), biopolimeri (PLA, alginato, gelatina, collagene), compositi **CFRP/CF-SMC** e leghe biomediche (**CoCr L605**).
  * Analisi di prove meccaniche a compressione (**ISO 13314**), tecniche di caratterizzazione chimico-fisica e morfologica superficiale (**SEM, AFM, FTIR, EDX**), cinetiche di degradazione *in vitro* (SBF, PBS, Tris-HCl) e protocolli regolatori di biocompatibilità (**saggio MTT**, **Test di Ames**, valutazione osteo-angiogenica).

---

## Contatti

* **Email:** [francesca.cognigni28@gmail.com](mailto:francesca.cognigni28@gmail.com) | [francesca.cognigni@studenti.unipd.it](mailto:francesca.cognigni@studenti.unipd.it)
* **GitHub:** [github.com/francescacognigni28-dotcom](https://github.com/francescacognigni28-dotcom)
* **Domicilio:** Padova (PD) | **Residenza:** Porto San Giorgio (FM)
