Symfony Standard Edition
========================

This is a Symfony project with the pourpose of creating a bundle for use
["blueimp/jQuery-File-Upload"][1] ().

il bundle che si vuole realizzare permette di gestire l'upload/cancellazione/download di file organizzandoli in cartelle (CollectionFl).
il download e la cancellazione dei file e' vincolato alle credenziali possedute dall'utente.

Quando il codice sara' maturo il codice e le funzionalita' implementate verrano migrate in un bundle in modo da semplificare il loro uso.


Entita' e Relazioni di jqFileUploadBundle
=========================================
Il bundle ha l'entita' CollectionFl che rappresenta una collezione di file.
i file rappresentati da un CollectionFl risiedono fisicamente in una cartella
il cui nome e' l'identificativo di CollectionFl.

@todo: Da comprensere se e' utile implementare anche un' entita' per i singoli file

Campi/proprieta' di CollectionFl:
-id


Entita' e Relazioni ausiliarie
==============================
per semplificare l'implementazione e creare una demo vengono introdotte
Altre entita' "ausiliarie":

filingCabinet--<fcContainsCfl>--CollectionFl

[filingCabinet][2] (armadio di fascicoli) che e' relazionato (molti a molti) con CollectionFl (fascicoli di file)
attraverso la relazione fcContainsCfl (filingCabinet-<Contains>-CollectionFl)

L'entita' fcContainsCfl ha le seguenti proprieta' (campi della tabella):
filingCabinet_id : identificativo di filingCabinet
CollectionFl_id : identificativo di CollectionFl
description: descrizione testuale




[1]:  https://github.com/blueimp/jQuery-File-Upload
[2]:  http://en.wikipedia.org/wiki/Filing_cabinet

