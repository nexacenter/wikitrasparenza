# Progetto Wikitrasparenza - Nexa Center for Internet and Society - Politecnico di Torino (DAUIN)

## Indice
Il seguente progetto è composto da:
1. Report "#WikiTrasparenza chi apre davvero i dati sulle risorse pubbliche"
2. Nota metodologica al report
3. Dati analizzati
4. Query SPARQL per interrogare la wiki
5. Dump CSV dei file presenti nella wiiki

## Report
Il report, in cui vengono esposti i risultati dell'analisi dei dati, è disponibile a questo indirizzo: http://nexa.polito.it/working-paper/2015-1

## Nota metodologica
Nella nota metodologica viene spiegato come è stata costruita la wiki semantica, come sono strutturati i dati, come è avvenuto il censimento dei dataset. disponibile su: http://nexa.polito.it/working-paper/2015-1

## Query SPARQL
Le query sparql per interrogare i dati della wiki sono nel file "Queries.SPARQL". L'endpoint SPARQL è presente all'indirizzo: https://trasparenza.nexacenter.org/sparql 
Altre query SPARQL specifiche sono presenti all'indirizzo: https://trasparenza.nexacenter.org/wiki/Query_sparql

## Dati analizzati
Sono stati analizzati 5 dataset per 119 Comuni capoluogo di Provincia o con più di 100 mila abitanti.
I 5 dataset analizzati analizzati riguardano ognuno un obbligo di pubblicazione stabilito dal d.lgs. n. 33/2013 e sono:
* Beni immobili e la gestione del patrimonio (Art. 30, d.lgs. n. 33/2013, di seguito “obbligo di pubblicazione beni immobili” )
	1. Patrimonio immobiliare
	2. Canoni di locazione attivi
	3. Canoni di locazione passivi
* Sovvenzioni, sussidi e contributi (Art.26-27 d.lgs. n. 33/2013, di seguito “obbligo di pubblicazione sovvenzioni”)
	4. Atti di concessione
	5. Albo dei beneficiari 

## Dump CSV
Sono disponibili i dump CSV dei dati presenti nella wiki. Ogni singolo file CSV rappresenta una categoria di dataset analizzati (Albo beneficiari, atti di concessioni, Locazioni attive, locazioni passive, patrimonio immobiliare). I dump sono i risultati delle queries esposte nel file "Queries.SPARQL".

Ogni file CSV è composto da diverse colonne. Le prime 5, comuni a tutti e 5 i dump, sono:
* dataset: URI alla wiki del dataset analizzato
* formato: formato del dataset analizzato
* URLdataset: URL del dataset analizzato, link al sito del Comune che l'ha pubblicato
* URLsezione: URL alla sezione della sezione trasparenza del Comune in cui è possibile scaricare il dataset analizzato
* tracciaRecordAttributi: annotazione degli attributi presenti nel dataset

Inoltre, per ogni dump sono presenti una serie attributi booleani (hanno valore o "0" o "1") che indicano la presenza o l'assenza di un determinato attributo in un determinato dataset analizzato, se il valore è "1" l'attributo è presente, se "0" è assente. 
Gli attributi del dump con queste caratteristiche hanno il nome composto in questo modo: "%nomeAttributo%PresenzaAttributo", ad esempio "DatiFiscaliBeneficiarioPresenzaAttributo" indica la presenza (o meno) dell'attributo "Dati fiscali del beneficiario". L'attributo dell'esempio è presente nel dump che raccoglie i dati sull'analisi dei dataset "atti di concessione".	
