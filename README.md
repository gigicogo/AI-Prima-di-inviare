# Prima di inviare — Laboratorio web sulla sicurezza dei prompt

Mini web app **offline, gratuita e statica** per la formazione del personale della Pubblica Amministrazione italiana. Include due esercizi individuali sulla minimizzazione dei dati e sulla scelta di un ambiente IA autorizzato.

## Avvio rapido

1. Scarica `index.html`.
2. Aprilo con un browser moderno (Chrome, Edge, Firefox o Safari).
3. Seleziona una delle due esercitazioni dalla pagina iniziale.

Non servono account, installazioni, connessioni Internet, API key o servizi esterni.

## Pubblicare con GitHub Pages

1. Crea un nuovo repository su GitHub.
2. Carica `index.html` e `README.md` nella **radice** del repository.
3. Apri **Settings → Pages**.
4. In *Build and deployment*, seleziona **Deploy from a branch**, quindi il branch principale (di solito `main`) e la cartella **`/ (root)`**.
5. Salva e apri l'indirizzo indicato da GitHub Pages quando la pubblicazione è pronta.

> Non occorrono workflow, build, Node.js o pacchetti npm. Il nome `index.html` è necessario per l'apertura automatica della pagina.

## Due esercizi

### 1. Il prompt sotto la lente (8–10 minuti)

**Scenario:** un ufficio deve preparare una sintesi generale delle difficoltà di prenotazione di uno sportello. Il testo «anonimizzato» e il file Word contengono ancora possibili identificatori.

**Attività:** per 8 elementi il partecipante deve decidere se **mantenere, rimuovere, generalizzare o fermare l'invio**. Il sistema controlla le scelte, mostra perché sono corrette o errate e impedisce di avanzare finché non sono affrontate tutte le criticità.

**Passaggio finale:** il partecipante valuta un testo ridotto e ottiene un *prompt didattico* riutilizzabile, soltanto dopo aver confermato tre verifiche preliminari.

**Messaggio didattico:** sostituire il nome con un codice non comporta necessariamente anonimizzazione. Anche nomi dei file, metadati, commenti e revisioni vanno esaminati.

### 2. Posso usare questo strumento? (8–10 minuti)

**Scenario:** un dipendente deve scegliere fra tre ambienti con autorizzazioni differenti: A, account personale non autorizzato per il lavoro; B, ambiente istituzionale autorizzato per determinate categorie di dati; C, servizio Enterprise con controlli dichiarati ma autorizzazione non verificata.

**Attività:** quattro casi documentali e una domanda finale. È possibile proseguire soltanto dopo aver scelto l'azione appropriata nel **contesto specifico della simulazione**.

**Messaggio didattico:** le dichiarazioni commerciali del fornitore non sostituiscono la valutazione e l'autorizzazione dell'ente.

## Come utilizzarla durante una lezione da remoto

- Invia ai partecipanti il link GitHub Pages o il file `index.html`.
- Dai **8–10 minuti** per il primo esercizio; il secondo è indipendente e può essere assegnato come approfondimento.
- Ogni persona lavora alla propria postazione: non occorrono gruppi o webcam.
- Al termine il partecipante può scaricare un **riepilogo `.txt`** e, se vuole, condividerne il punteggio o i criteri emersi durante la discussione.
- Il formatore può chiedere in chat: «Quale elemento sembrava innocuo ma non lo era?» e «Perché una licenza Enterprise non basta?».

## Funzionalità

- Correzioni contestuali immediate e possibilità di riprovare.
- Avanzamento vincolato alla soluzione delle criticità.
- Indicatore delle risposte corrette al primo tentativo (non è un attestato di competenza).
- Download di un riepilogo `.txt`.
- Layout responsive e controlli accessibili da tastiera.
- Nessuna raccolta o trasmissione di dati: non ci sono analytics, cookie di tracciamento, API esterne o database.
- Lo stato rimane in memoria nella scheda del browser: **ricaricando la pagina si ricomincia**.

## Limiti importanti

I documenti, i dipendenti, gli uffici e le autorizzazioni descritte sono **interamente fittizi**. La web app **non esegue anonimizzazione reale**, **non verifica contratti**, **non autorizza strumenti**, **non contatta modelli IA** e non certifica conformità al GDPR o ad altre norme.

Le risposte corrette valgono nel **contesto didattico esplicitato nelle schermate**. Nella pratica ogni amministrazione deve attenersi alle proprie policy, alle autorizzazioni, alla valutazione della finalità e al quadro normativo applicabile. La pseudonimizzazione non equivale automaticamente all'anonimizzazione.

**Non inserire dati personali o documenti reali nell'app.** Tutti gli esempi forniti sono simulati.

## Personalizzazione e riuso

L'interfaccia, i contenuti e la logica sono inclusi nel solo `index.html`. Per cambiare casi, testi o scelte corrette, modifica rispettivamente gli array JavaScript `choices`, `cases` ed `environments` dentro il file; quindi ricarica la pagina.

Il materiale è pensato per essere riutilizzabile presso amministrazioni diverse, senza riferimenti a un ente specifico.

## Struttura dei file

```text
prima-di-inviare/
├── index.html              # App autonoma (HTML + CSS + JavaScript)
├── README.md               # Istruzioni, installazione e limiti
└── GUIDA_FORMATORE.md      # Chiavi e suggerimenti per la conduzione
```

> La guida del formatore contiene le soluzioni: se il repository è pubblico, considerare di conservarla separatamente o di non pubblicarla, distribuendola soltanto al docente.
