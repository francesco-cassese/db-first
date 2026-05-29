# Concessionario Auto Usate

## Schema tabella `veicoli`

| Nome Colonna | Tipo | Attributi | Index |
| --- | --- | --- | --- |
| **id** | UNSIGNED INT | NOT NULL AUTO INCREMENT | PRIMARY KEY|
| **brand** | VARCHAR(50) | NOT NULL | INDEX |
| **modello** | VARCHAR(50) | NOT NULL | |
| **prezzo** | DECIMAL(10,2)| NOT NULL | INDEX |
| **anno_Immatricolazione** | YEAR | NOT NULL | 
| **km_percorsi** | UNSIGNED MEDIUMINT| NOT NULL | INDEX |
| **numero_proprietari** | UNSIGNED TINYINT | DEFAULT(1) | | 
| **tipo_cambio**| VARCHAR(20)| DEFAULT('manuale')| INDEX |
| **tipo_alimentazione** | VARCHAR(30) | NOT NULL | INDEX |
| **potenza_kw** |UNSIGNED SMALLINT | NOT NULL | |
| **data_ultima_revisione** | DATE | NULL | 