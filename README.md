# Concessionario Auto Usate

## Schema tabella `vehicles`

| Nome Colonna | Tipo | Attributi | Index |
| --- | --- | --- | --- |
| Id | UNSIGNED INT | NOT NULL AUTO INCREMENT | PRIMARY KEY|
| Brand | VARCHAR(50) | NOT NULL | INDEX |
| Modello | VARCHAR(50) | NOT NULL | |
| Prezzo | DECIMAL(10,2)| NOT NULL | INDEX |
| Anno_Immatricolazione | YEAR | NOT NULL | 
| Km_percorsi | UNSIGNED MEDIUM INT| NOT NULL | INDEX |
| Numero_proprietari | UNSIGNED TINY INT | DEFAULT(1) | | 
| Tipo_alimentazione | VARCHAR(30) | NOT NULL | INDEX |
| Data_Ultima_Revisione | DATE | NULL | |