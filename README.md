# Sito Valentina Angeli — Istruzioni

## 1. Carica i file su GitHub
1. Vai sul tuo account GitHub → crea un nuovo repository (es. `sito-valentina`), pubblico.
2. Carica dentro TUTTI i file e le cartelle di questo pacchetto (trascinali dal browser
   nella pagina "Add file → Upload files").
3. Vai su **Settings → Pages** del repository, in "Branch" scegli `main` e cartella `/ (root)`, salva.
4. Dopo 1-2 minuti il sito sarà online su:
   `https://TUOUSERNAME.github.io/sito-valentina/`

## 2. Configura username e repo
Apri il file `js/config.js`, e sostituisci:
```
GITHUB_OWNER: "INSERISCI-USERNAME",   → il tuo username GitHub
GITHUB_REPO:  "INSERISCI-NOME-REPO",  → il nome del repository che hai creato
```
Salva e ricarica su GitHub (puoi modificare il file direttamente sul sito di GitHub,
con la matita in alto a destra quando apri il file).

## 3. Genera il token per l'admin foto
1. Su GitHub vai su **Settings del tuo account** (non del repo) → **Developer settings**
   → **Personal access tokens** → **Fine-grained tokens** → **Generate new token**.
2. Dai un nome (es. "admin sito Valentina"), scadenza a piacere (es. 1 anno).
3. In "Repository access" scegli "Only select repositories" → seleziona il repo del sito.
4. In "Permissions → Repository permissions" imposta **Contents: Read and write**.
5. Genera il token e **copialo subito** (non lo rivedrai più).
6. Questo token va incollato nella pagina admin ogni volta che vuoi caricare foto —
   non va condiviso con nessuno, è come una password.

## 4. Pagina admin
La pagina admin è raggiungibile solo da chi ha il link diretto:
`https://TUOUSERNAME.github.io/sito-valentina/admin.html`
Non è collegata dal sito pubblico e ha il tag `noindex` per non finire su Google.
Condividi questo link solo con chi deve caricare le foto (tu/Valentina).

## 5. Form di contatto (Formspree)
Il form usa Formspree (gratuito fino a 50 messaggi/mese):
1. Vai su https://formspree.io → crea un account gratuito.
2. Crea un nuovo form, copia l'ID che ti danno (tipo `xzbqrwka`).
3. In `index.html`, cerca la riga:
   `action="https://formspree.io/f/INSERISCI-ID-FORMSPREE"`
   e sostituisci `INSERISCI-ID-FORMSPREE` con l'ID copiato.
4. I messaggi arriveranno all'email con cui ti sei registrato su Formspree.

## 6. Contenuti da rivedere con Valentina
Ho scritto una bozza di testi — vanno confermati/corretti:
- Bio nella sezione "Chi sono"
- Elenco servizi (sono generici, da adattare a cosa offre davvero)
- Indirizzo esatto, orari, telefono, email, P.IVA (footer)
- Foto profilo e foto dello studio (caricabili da admin.html)

## Struttura file
```
index.html              → sito pubblico
admin.html               → pannello caricamento foto (link privato)
css/style.css             → stile e animazioni
js/config.js              → username/repo GitHub (da compilare)
js/main.js                → logica sito pubblico
js/admin.js                → logica pannello admin
images/gallery/             → dove finiscono le foto caricate
images/gallery-manifest.json → elenco foto (gestito in automatico)
```
