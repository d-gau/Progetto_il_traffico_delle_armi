# Progetto_il_traffico_delle_armi
Descrizione del Progetto
Questo progetto applica tecniche di Data Science e Network Analysis ai dati del commercio internazionale di armi (SIPRI, 1950-2023). L'obiettivo va oltre la semplice quantificazione dei volumi di vendita: il progetto mira a svelare la struttura delle alleanze geopolitiche, misurando l'influenza strategica e la dipendenza tra le nazioni.

## Analisi e Conclusioni: I 5 Pilastri del Progetto
Il lavoro si articola in 5 fasi con le rispettive domande che mi sono posto e le conclusioni che ho tratto dall'analisi dei dati. Di seguito sono riportate le metodologie utilizzate e le conclusioni tratte dai dati.

#### Domanda 1 - La Struttura della Rete Globale (Network Construction)
   
   Il mondo è stato modellato come un grafo diretto pesato, dove i nodi sono gli Stati e gli archi rappresentano i flussi di armi misurati in TIV (Trend Indicator Value, l'unità di misura del valore militare   strategico dei vari armamenti).

  Domanda: Com'è strutturato il mercato bellico globale?

  Conclusione: La rete è fortemente asimmetrica e gerarchica. Esiste un ristretto numero di "Hub" (fornitori primari) che serve una vasta platea di "Customers" (clienti). La topologia della rete suggerisce che pochi attori controllano la maggioranza della tecnologia militare avanzata, creando colli di bottiglia strategici.

#### Domanda 2 - Identificazione delle Fazioni (Community Detection)

  Utilizzando l'algoritmo di clustering Walktrap, i paesi sono stati raggruppati automaticamente in "comunità" basate sull'intensità e la direzione degli scambi.

  Domanda: Si possono individuare dei blocchi geopolitici?

  Conclusione: L'algoritmo rileva una polarizzazione netta:
  - Blocco Blu: Guidato dagli USA e dai paesi NATO.
  - Blocco Rosso: Una sfera d'influenza gravitante attorno alla Russia e in parte alla Cina.
  
  Controllando gli schieramenti e prodotti da questa analisi, mi sono reso conto che la divisione delle allenaze non corrispondeva con le mie conoscenze. Questo accade perchè il periodo preso in esame può essere diviso in due macroperiodi in cui le alleanze cambiano in modo significativo: la Guerra Fredda (1950 - 1991), post-patto di Varsavia fino ai nostri giorni.
  Pertanto ho deciso di rianalizzare i dati in queste 2 finestre temporali. 

Notatndo che anche utilizzando la data del Patto di Varsavia gli schiermaenti non mi risultavano coerenti con la mia consocenza della storia delle relazioni internazionali, ho provato a ridividere i dati in pre e post Trattato di Parigi (1997). In questo modo i dati forniscono delle fazioni più vicine a quelle che sono relamente esistite. D'altronde sono serviti degli anni per ridefinire gli equilibri geopolitici e gli scambi internazionali

#### Domanda 3 -  La Misurazione del Potere 

   È stata implementata una funzione ricorsiva per calcolare il potere di ogni Nazione, una metrica che definisce il potere non in base al volume totale di vendita, ma in base alla dipendenza esclusiva dei propri clienti.
   Domanda: Chi detiene il vero potere strategico?
   Conclusione: Un fornitore è potente se i suoi clienti non hanno alternative.
   - I dati mostrano che la Russia mantiene un indice di potere elevato rispetto al volume di armi scambiate.
   - Gli USA, pur dominando i volumi, servono clienti più "connessi" (es. Europa), diluendo parzialmente il punteggio di "monopolio puro".

#### Domanda 4 - Analisi Temporale: I Cicli del Riarmamento

Attraverso l'analisi delle serie storiche dei flussi TIV (1950-2023), il progetto mappa l'evoluzione della tensione globale.
   Domanda: Quando si verificano i picchi di scambio?
   Conclusione: Il mercato delle armi agisce come un sismografo delle relazioni internazionali.
   Possiamo individuare 3 picchi:
   - Anni '80: Il picco più alto (tensioni della Guerra Fredda, guerra Iran-Iraq);
   - Anni 2000: L'aumento di armi in seguito all'attentato dell'11 settembre;
   - 2014: Guerra di Crimea.

#### Domanda 5 - Analisi dei Conflitti Attuali (Case Studies: Israele & Ucraina)

Un focus specifico è dedicato ai teatri di guerra attivi, analizzando i registri di commercio verso Israele e Ucraina.

Domanda: Con le armi di chi si combattono le guerre di oggi?

Conclusione: L'analisi qualitativa dei mezzi rivela che il sostegno moderno non è solo "ferro" (carri armati), ma sempre più "precisione" (bombe guidate, difesa aerea, sensoristica). Questo rende i belligeranti dipendenti non solo dalla fornitura iniziale, ma dal flusso continuo di munizionamento e supporto tecnico degli alleati.
