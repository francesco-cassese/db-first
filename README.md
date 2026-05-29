# Concessionario Auto Usate

## Schema tabella `veicoli`

| Nome Colonna | Tipo | Attributi | Index |
| --- | --- | --- | --- |
| **id** | UNSIGNED INT | NOT NULL AUTO INCREMENT | PRIMARY KEY|
| **brand** | VARCHAR(50) | NOT NULL | INDEX |
| **modello** | VARCHAR(50) | NOT NULL | |
| **prezzo** | DECIMAL(10,2)| NOT NULL | INDEX |
| **anno_Immatricolazione** | YEAR | NOT NULL | 
| **km_percorsi** | UNSIGNED MEDIUM INT| NOT NULL | INDEX |
| **numero_proprietari** | UNSIGNED TINY INT | DEFAULT(1) | | 
| **tipo_alimentazione** | VARCHAR(30) | NOT NULL | INDEX |
| **data_ultima_revisione** | DATE | NULL | 