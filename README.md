# DeutschCards — pagine legali (GitHub Pages)

Stesso schema di Kegel Flow (`simone-dev19/kegel-flow-legal`): un repository pubblico separato, solo con le pagine che Apple vuole a un indirizzo pubblico. Il codice dell'app resta nel repository privato.

Indirizzi una volta pubblicato:

- Informativa privacy: `https://simone-dev19.github.io/deutschcards-legal/privacy-policy-it` (e `-en`)
- Supporto: `https://simone-dev19.github.io/deutschcards-legal/support`

L'app (`www/index.html`, costante `PRIVACY_URL`) e le schede store (`store/listing_*.md`) puntano già a questi indirizzi.

## Pubblicare (una volta sola, dal Terminale del Mac)

```bash
gh auth login --hostname github.com --git-protocol https --web   # entrare come simone-dev19
cd ~/Documents/Claude-Projects/deutschcards-legal
git init -b main && git add -A && git commit -m "Pagine legali DeutschCards"
gh repo create simone-dev19/deutschcards-legal --public --source . --push
gh api -X POST repos/simone-dev19/deutschcards-legal/pages -f 'source[branch]=main' -f 'source[path]=/'
```

Dopo uno o due minuti le pagine sono online (pubblicate il 5 ottobre 2026).

## Aggiornare le pagine

Sul Mac Studio `gh` ha due account (`simon-act` per il repository dell'app, `simone-dev19` per queste pagine) e nel portachiavi è salvata la credenziale di `simon-act`: un `git push` semplice viene rifiutato con errore 403. Usare:

```bash
gh auth switch --user simone-dev19
cd ~/Documents/Claude-Projects/deutschcards-legal
git add -A && git commit -m "Aggiornamento pagine"
git -c credential.helper= -c credential.helper='!gh auth git-credential' push
```

In questa cartella nome ed email di git sono già impostati sull'indirizzo anonimo di `simone-dev19`. Per tornare a lavorare sul repository dell'app: `gh auth switch --user simon-act`.
