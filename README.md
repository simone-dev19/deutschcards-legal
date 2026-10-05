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

Dopo uno o due minuti le pagine sono online. Per aggiornarle: modifica i file, `git commit`, `git push`.
