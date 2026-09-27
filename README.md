# ASD Il Sentiero

Sito statico dell'associazione, pubblicato con GitHub Pages.

## Aggiornare i contenuti

Le pagine del sito sono file Markdown nella cartella principale:

- `index.md` — home page
- `associazione.md` — associazione, direttore tecnico e insegnanti
- `sedi.md` — le tre sedi dei corsi
- `discipline.md` — Tai Chi Chuan, Qi Gong e Ba Gua Zang
- `iniziative-eventi.md` — archivio delle iniziative
- `contatti.md` — riferimenti dell'associazione

Per pubblicare una nuova iniziativa, creare un file Markdown nella cartella
`_events`, seguendo il modello `_events/_template.md`. Gli eventi con una data
futura compariranno prima nell'elenco.

Ogni modifica deve essere proposta con una pull request: la pubblicazione su
GitHub Pages parte automaticamente solo dopo l'unione in `main`.

## Anteprima locale (facoltativa)

Con Ruby e Bundler installati:

```powershell
bundle install
bundle exec jekyll serve
```

L'anteprima sarà disponibile a `http://localhost:4000/il-sentiero/`.
