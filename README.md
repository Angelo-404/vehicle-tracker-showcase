# App gestione veicolo

Il codice di questo progetto è privato. Qui racconto cosa fa e come è costruito.

## Cosa fa

È un'app per Android e iOS che tiene sotto controllo un veicolo, e funziona anche senza rete perché i dati restano
sul telefono.

Le scadenze di revisione e bollo si calcolano da sole partendo dalla data di immatricolazione, con le regole italiane;
quella dell'assicurazione si legge dalla foto della polizza. Si registrano rifornimenti, consumi, spese anche
ricorrenti, manutenzione programmata e gomme, e l'app calcola quanto costa davvero il veicolo al chilometro. Ci sono
i prezzi dei carburanti dai dati pubblici del Ministero, la lettura con la fotocamera di libretto e fatture, i
viaggi registrati col GPS, i comandi vocali, una sezione per le emergenze con la constatazione amichevole, l'import
dei dati da Fuelio e il backup.

## Come è costruito

Expo e React Native con TypeScript in modalità stretta. I dati stanno in un database SQLite sul telefono, gestito con
Drizzle ORM e migrazioni incluse nell'app. Le regole di calcolo stanno in funzioni pure separate dall'interfaccia,
così si possono provare da sole. I testi che vede l'utente sono in un file a parte.

## Come l'ho verificato

Test automatici con Jest sulle regole di calcolo; controllo dei tipi, lint e test girano insieme con un solo comando.

## Stato

Provata su emulatore, non ancora pubblicata sugli store.
