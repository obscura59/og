# Installazione

Quando OG viene installato, appaiono anche due nuovi **tipi di contenuto** (_content type_): **Group** e **Contenuto** (_Group_ e _Post_).

Il tipo di contenuto _group_ serve a definire (ma và!) un gruppo: nel nostro caso definirà una sezione all'interno dell'area riservata, mentre _contenuto_ servirà a aggiungere del contenuto all'interno del gruppo.

Quando il modulo OG viene attivato, nel modulo di creazione di un content type appare una nuova tab verticale, Group. Questa tab consente di definire un tipo di contenuto o come un Gruppo, o come un contenuto di gruppo, oppure nessuno di questi.

# Cos'è un Gruppo?

In D7, qualunque _entity_ può essere un gruppo e qualunque _entity_ può far parte di un gruppo. Un gruppo è composto di molte differenti tipi di **entità** (_entity_). Al centro di tutto c'è il gruppo stesso, che, il più delle volte, è un nodo. Un **Gruppo** è, per così dire, il _"genitore"_ per tutte le diverse _"cose"_ che appartengono a un gruppo.

Utenti e contenuto sono due tipi di _entities_ che possono appartenere a un gruppo. Ciascun utente e ciascun contenuto sono connessi al gruppo (o ai gruppi) di apprtenenza per il tramite di un entity addizionale. Questa _entity_ è una **particolare iscrizione OG** che collega utenti e contenuti con i gruppi cui sono associati. Ad alto livello, è semplicemente un record in una tabella del database, che tiene traccia di quali _entities_ sono associate a quali gruppi.

## Group Entities

Per iniziare con **OG**, dobbiamo decidere che tipo di entity sarà il _"genitore"_; in Drupal 7 nnon deve essere necessariamente un nodo, ma può essere qualunque tipo di entità; sebbene nella maggioranza dei casi sarà comunque un tipo di contenuto (_content type_), questo non è un obbligo; per esempio di potrebbero usare dei termini di tassonomia (_taxonomy terms_) come Gruppo.

## Group Content Entities

Il contenuto di un gruppo non è limitato a un nodo o a un tipo di contenuto. Altri tipi di _entities_ possono appartenere a un gruppo. Le entità disponibili a appartenere a (far parte di) un gruppo dipendono solo dai moduli installati sul sito. Per esempio, se è installato il modulo [media](https://www.drupal.org/project/media), allora il tipo di entità _media_ può far parte di un gruppo. Se è installato [commerce](https://www.drupal.org/project/commerce), i _prodotti_ possono far parte di un gruppo. Inoltre, dato che, come abbiamo visto, **qualunque _entity_ può definire un gruppo**, ciascuna di queste _entities_ può essere usata come _Group Entity_.

Gli utenti sono un'ltro, particolare, tipo di _group 'content' entity_. Gli utenti sono collegati al gruppo nello stesso modo con cui sono connessi i contenuti, cioè con una _entità iscrizione OG_; in più essi hanno alcune speciali proprietà, in quanto gli utenti possono avere dei ruoli loro assegnati e fruire di permessi che controllano quello che possono fare all'interno di un gruppo.

Dato che qualunque tipo di _entity_ può appartenere a un gruppo, uno stesso gruppo può essere il _contenuto_ di un altro gruppo. Questo permette di avere gruppi che contengono altri gruppi, cioè si possono creare dei sottogruppi.

# Caratteristiche

- I gruppi possono essere creati sia dagli admin, sia dagli utenti stessi (purché autorizzati);
- I gruppi possono avere dei ruoli loro propri (admin, editor, etc.);
- I permessi vengono assegnati a questi ruoli, **a livello di gruppo**;
- Gli amministratori assegnano i ruoli a livello di gruppo ai membri del gruppo;
- L'iscrizione a un gruppo può essere libera o moderata;
- L'inserimento di contenuti all'interno di un gruppo può essere controllata tramite i permessi;
- L'accesso al contenuto postato in un gruppo può essere limitato ai soli membri di quel gruppo.
