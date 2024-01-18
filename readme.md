# DB First

## Assignment

Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario.

## Description

### ID

Questo tipo di dato descrive l'identificativo dell'auto, è univoco e auto-incrementale (parte da zero e ad ogni elemento inserito aumenterà di +1).

### Brand

La marca dell'auto, ho scelto di usare _VARCHAR_ perché sia variabile e perché 20 caratteri possono bastare a descrivere la marca.

### Model

Il modello dell'automobile, ho scelto _VARCHAR_ per la variabilità e perché sempre 20 caratteri possono bastare.

### Price

Il prezzo della macchina. Ho preso come paragone l'ordine di 10^6 euro, più 2 virgole decimali precise come si vede normalmente nei prezzi.

### KM

I chilometri percorsi dall'automobile, _MEDIUMINT_ mi è sembrata la scelta più sensata (255 di TINYINT e SMALLINT sono troppo poco).

### Production_year

In questo caso viene descritto l'anno di produzione originale della macchina, usando _YEAR_ poiché ci interessa appunto solamente l'anno e non tutto il timestamp.

### Description

Questa è una descrizione generale delle caratteristiche dell'auto. Usando _TEXT_ ci assicuriamo che la memoria messa a disposizione basti per accogliere un semplice test di descrizione.

### Database_placement

La data precisa di inserimento della macchina nel database del concessionario. Qui invece di year usiamo _DATE_ perché vogliamo ottenere più informazioni.

### Is_available

Qui stiamo chiedendo se l'auto è disponibile nel concessionario. Siccome sarà un sì/no ho scelto di usare un valore booleano, rappresentato con _TINYINT_ poiché basterà uno 0/1 per discernere true da false.

### Fuel_type

La tipologia di carburante utilizzato dall'auto: _VARCHAR(20)_ è abbastanza per avere una variazione sufficiente dei vari tipi.

### Color

Il colore della macchina: pur non essendo future proof, mi è sembrato che 20 sia sufficiente come lunghezza massima.

### Plate

Per la targa della macchina ho scelto di usare _CHAR(7)_ perché sappiamo che le targhe italiane hanno 7 caratteri, e questo concessionario è situato in Italia.
