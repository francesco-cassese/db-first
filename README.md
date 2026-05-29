# 🚗 Esercitazione: Concessionario Auto Usate
 **nome repo:** `db-first`

**🎓 Nota:** Questo documento presenta l'esercitazione di modellazione database per un sistema di gestione auto usate, svolta a fini didattici.

## 📝 Obiettivo
L'obiettivo di questa esercitazione è definire una struttura dati ottimizzata per gestire l'inventario di un concessionario di auto usate, focalizzandosi sulla corretta tipizzazione dei dati e sull'indicizzazione.

## 🗄️ Schema Tabella: `veicoli`
Di seguito è riportata la struttura tecnica della tabella utilizzata per memorizzare le informazioni di ogni automobile.

| Nome Colonna | Tipo | Attributi | Index |
| --- | --- | --- | --- |
| **id** | UNSIGNED INT | NOT NULL AUTO INCREMENT | PRIMARY KEY|
| **brand** | VARCHAR(50) | NOT NULL | INDEX |
| **modello** | VARCHAR(50) | NOT NULL | |
| **colore** | VARCHAR(30) | NOT NULL | INDEX |
|**url_immagine** | VARCHAR(255) | DEFAULT('placeholder.png') | |
| **prezzo** | DECIMAL(10,2)| NOT NULL | INDEX |
| **anno_immatricolazione** | YEAR | NOT NULL | 
| **chilometraggio** | UNSIGNED MEDIUMINT| NOT NULL | INDEX |
| **numero_proprietari** | UNSIGNED TINYINT | DEFAULT(1) | | 
| **tipo_cambio**| VARCHAR(20)| DEFAULT('manuale')| INDEX |
| **tipo_alimentazione** | VARCHAR(30) | NOT NULL | INDEX |
| **potenza_kw** |UNSIGNED SMALLINT | NOT NULL | |
| **data_ultima_revisione** | DATE | NULL | 


## 🛠️ Note tecniche
**Performance:** Abbiamo applicato degli indici (INDEX) sulle colonne più frequenti nelle query di ricerca (come brand, prezzo e chilometraggio) per garantire risposte rapide. ⚡

**Integrità dei dati:** L'uso di tipi numerici UNSIGNED evita il salvataggio di dati non validi (numeri negativi), ottimizzando anche lo spazio di archiviazione. 💾

**User Experience:** Il campo url_immagine assicura che il sistema non vada in errore in caso di mancanza di una foto, utilizzando un'immagine di fallback. 🖼️