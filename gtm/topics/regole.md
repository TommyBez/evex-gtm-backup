# Regole permanenti

Tutte le regole date da Tommy o registrate dopo un incidente. Ogni regola porta data e origine.
Parte del grafo gtm: indice in [../STATE.md](../STATE.md).

## Processo

- **Merge e pubblicazioni esterne solo Tommy.** I run aprono PR, mai commit su main.
- **Sit è morta** (26/08 ~19:03 CEST). Crescita piattaforma: SEO + agenti first-party nuovi. Non defaultare a hold.
- **Lennybot è fuori** (26/08). PMM possiede la strategia da sola. Non consultarlo, non aspettare un consulto.
- **PMM sceglie slug e pagine.** Non rimbalzare a Tommy le scelte tattiche (20/08, riaffermato).
- **Commenti PR: sempre, senza che Tommy lo dica** (20/08, 26/08). Soft Eng sweep immediato su CodeRabbit / Codex / umani.
- **Voce verso Tommy e Slack** (18/08, 20/08, 28/08): frasi intere. Cosa è successo, perché conta, cosa deve fare. Mai telegrafico, mai aprire con numeri di PR o dump di metriche. Lui non legge le chat CoS con PMM / SEO / Soft Eng.
- **Mai dire che il Mac è offline** (20/08) se un write su `gtm/` fallisce. Riprovare. Il problema è il tool, non la sua macchina.
- **Niente paid ads, niente sales** (17/08). Core: Chief of Staff, Soft Eng, PMM, SEO.

## Copy e install

- Comando di install **sempre** `npx shadcn@latest add @evex/<slug>`. Mai `eve add https://www.evex.sh/r/<slug>.json` in copy, OG, Typefully, meta (12/08; una nota dell'11/08 che dava eve add come sostituto è SUPERATA).
- In listing e social l'esempio è generico `@evex/<slug>`, non `@evex/code-reviewer` (19/08). code-reviewer può restare demo in homepage.
- **Su X** il comando si scrive `npx shadcn@latest add [@]evex/<slug>` così X non menziona un profilo @evex (21/08, Tommy ha messo le parentesi lui). Fuori da X (sito, docs, listing, bozze Typefully non ancora editate) resta `@evex/<slug>`. Un `[@]` su un post X già uscito non è un bug e non si chiede di cancellare/ripubblicare.
- LinkedIn in italiano, X in inglese (10/08).
- Mai em dash nella copy pubblica (social ed editoriale). Sui repo di terzi (directory PR, awesome list) si segue lo stile della casa, anche con em dash (14/08).
- Niente frasi fatte da AI (10/08).
- Ogni bozza Typefully ha un **commento** con data/ora suggerita e una riga di motivazione (10/08).
- **Mai «Not a PR reviewer»** (o lo stesso contrasto-con-code-reviewer) come chiusura di default sui post X (27/08). Dire cosa fa l'agente nuovo.
- Job-intent title sulle pagine agente first-party può sforare il budget 60 caratteri di proposito. Vince la copy di prodotto; il layout aggiunge ` · evex`. Non accorciare per il cap (28/08).
- Niente helper sotto il comando Copy (20/08, override Tommy + lock PMM). Bottone `Copy command`. Hero resta code-reviewer finché PMM non dice altro.

## North star

- Evento `agent_install_command_copied`. Superfici: `sticky_install_cta` OR `mobile_install_bar` OR `install_command` (19/08). Guardare solo sticky perde il telefono.
- Se `viewer_is_author` manca e la persona non è loggata, conta come non-autore (20/08). Escludere i test team noti (Soft Eng sticky 19/08 19:27 UTC).
- Non twittare una copy della north star se PMM l'ha lockata come score-only (es. OpenUI 30/08).

## SEO e agenti

- Strategia SEO: playbook/skill di Search Counsel, o review sua. PMM resta owner del play. Search Counsel è consulente, non un posto fisso (26/08).
- Ispezione GSC UI (request indexing) è un click manuale, non c'è API. Login: `tommaso.carnemolla@gmail.com`. Non productbuild, non tommyrotten. Di default i run usano il service account in sola lettura e **non** fanno login UI a meno che Tommy non chieda quel click.
- **Prossimo agente first-party pubblicato: non un altro job GitHub** (28/08). Esplorare la superficie Eve. `linear-cycle-digest` resta morto. `@evex/support-reply-draft` (30/08) è quell'agente.
- Titoli/lede job-intent: PMM locka il copy, Soft Eng non ricopia da solo.

## Curl e bot

- Ogni curl nudo verso `/r/*` viene contato come install. Nelle verifiche usare UA con marker bot, es. `curl -A "evex-gtm-check-bot"`.
