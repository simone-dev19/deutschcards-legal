# Registro lavori AI — deutschcards-legal

Ogni voce descrive un intervento di un agente AI in questa cartella. Le voci più recenti sono in fondo. Formato e regole: vedi `AGENTS.md`.

## Storico ricostruito (scritto il 2026-10-05 da Claude)

> Nessun lavoro precedente: la cartella è stata creata con la voce qui sotto.

---

## 2026-10-05 15:24 — Creazione delle pagine pubbliche di DeutschCards

**Agente:** Claude (Cowork) · Claude Opus 5.5

**Richiesta:** allineare DeutschCards a Kegel Flow per informativa privacy e supporto.

**Cosa ho fatto:** creata la cartella sullo schema di `app-development/marketing/legal` (Kegel Flow): stesso `_config.yml` (tema minimal, `permalink: /:basename`), pagina indice, informativa in italiano e in inglese, pagina di supporto con domande frequenti. Niente termini di servizio: l'app è gratuita, senza account né acquisti, e Apple non li richiede.

**File toccati:**
| Azione | Percorso (relativo alla cartella) | Note |
|---|---|---|
| creato | `_config.yml`, `index.md`, `privacy-policy-it.md`, `privacy-policy-en.md`, `support.md` | pagine del sito |
| creato | `README.md`, `AGENTS.md`, `LOG_AI.md` | esclusi dal sito |

**Risultati:** niente è online. La cartella non è ancora un repository git.

**Decisioni di Simone:** account GitHub `simone-dev19`, non `simon-act`.

**Da sapere / aperto:** pubblicare con i comandi del README (serve entrare in `gh` come `simone-dev19`). Indirizzi previsti: `https://simone-dev19.github.io/deutschcards-legal/privacy-policy-it`, `…-en`, `…/support`. L'email mostrata è `simonepirovanog@gmail.com`.

**Sessione:** https://claude.ai/code/session_01EKQwYy7Ub1A9SZscyVEZFu

---

## 2026-10-05 15:34 — Push su GitHub e pagine legali online

**Agente:** Claude (Cowork) · Claude Opus 5.5

**Richiesta:** pubblicare il lavoro del 5 ottobre.

**Cosa ho fatto:** niente sui file. I comandi li ha lanciati Simone dal Terminale; l'agente ha verificato gli indirizzi.

**File toccati:**
| Azione | Percorso (relativo alla cartella) | Note |
|---|---|---|
| modificato | `LOG_AI.md` | questa voce (non ancora in commit) |

**Risultati:**
- `simon-act/deutschcards`: push di `main` da `a19dc25` a `10bb664` (progetto iOS, modifiche all'app, store, screenshot).
- `simone-dev19/deutschcards-legal`: repository pubblico creato, commit `6eb33cf`, GitHub Pages attivo su `main` /.
- Verificati online e funzionanti: `https://simone-dev19.github.io/deutschcards-legal/`, `/privacy-policy-it`, `/privacy-policy-en`, `/support` (email `simonepirovanog@gmail.com`, data 5 ottobre 2026). Il link privacy dentro l'app ora porta a una pagina esistente.

**Da sapere / aperto:** `gh` ha due account: `simon-act` (repository dell'app) e `simone-dev19` (pagine legali), si cambia con `gh auth switch --user <nome>`; dopo questa pubblicazione è attivo `simone-dev19`. Il commit delle pagine legali ha come autore l'identità automatica del Mac (`simonepirovano@simones-mac-studio.home`), visibile nel repository pubblico. Restano: app su App Store Connect, Archive in Xcode, scheda store, invio.

**Sessione:** https://claude.ai/code/session_01EKQwYy7Ub1A9SZscyVEZFu
