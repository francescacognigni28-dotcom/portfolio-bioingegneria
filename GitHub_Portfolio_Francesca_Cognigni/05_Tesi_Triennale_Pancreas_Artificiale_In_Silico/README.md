# Il Sistema Pancreas Artificiale e la sua Validazione In Silico

**Tesi di Laurea Triennale in Ingegneria Biomedica (Interclasse L-8 / L-9)**  
**Università degli Studi di Padova** – Dipartimento di Ingegneria dell'Informazione (Novembre 2024)  
**Relatore:** Prof. Simone Del Favero | **Laureanda:** Francesca Cognigni  
📄 **[Visualizza la Tesi Completa (PDF)](./Tesi_Triennale_Pancreas_Artificiale_Validazione_In_Silico.pdf)**

---

## Abstract e Obiettivo

Il diabete mellito di tipo 1 (T1D) è una patologia autoimmune cronica caratterizzata dalla distruzione delle cellule $\beta$ pancreatiche, che richiede la somministrazione quotidiana di insulina esogena per mantenere la glicemia nell'intervallo euglicemico ($70\text{–}180\text{ mg/dl}$).

L'elaborato di tesi analizza l'architettura ingegneristica dei moderni sistemi di **Pancreas Artificiale (AP)** a catena chiusa (*closed-loop*) e approfondisce il ruolo cruciale della **modellazione matematica fisiologica e della simulazione *in silico*** nella progettazione, taratura e validazione preclinica degli algoritmi di controllo automatico, riducendo i tempi, i costi e i rischi etico-clinici della sperimentazione *in vivo*.

---

## Struttura Tecnica del Lavoro

1. **Modellazione Matematica del Sistema Glucosio-Insulina:**
   * Analisi della rete fisiologica di regolazione glicemica e formulazione matematica a compartimenti del sottosistema del glucosio, del sottosistema dell'insulina e dei processi unitari (produzione epatica endogena, assorbimento gastrointestinale dei pasti, utilizzazione insulino-dipendente e insulino-indipendente, escrezione renale, cinetica di assorbimento sottocutaneo dell'insulina).
2. **Il Simulatore del Diabete di Tipo 1 UVA/Padova:**
   * Architettura del **simulatore UVA/Padova** (primo modello *in silico* approvato dalla **FDA** statunitense in sostituzione dei trial preclinici su modello animale per il test di strategie terapeutiche nel diabete di tipo 1).
   * Popolazione virtuale (*in silico subjects* adulti, adolescenti e bambini), modellazione degli errori del sensore sottocutaneo e della dinamica del microinfusore.
3. **Componenti Hardware e Algoritmi del Pancreas Artificiale:**
   * Sensori per il monitoraggio continuo del glucosio (**CGM**), pompe di infusione sottocutanea continua di insulina (**CSII**) e architetture degli algoritmi di controllo automatico (*PID – Proportional-Integral-Derivative* e *MPC – Model Predictive Control*), con analisi delle evidenze cliniche sul miglioramento del *Time in Range* (TIR) e sulla riduzione degli eventi ipoglicemici.
