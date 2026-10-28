# Changelog

## 1.2.0 — 2026-10-27
- **Mappa a scelta dall'admin**: Google Maps (come prima, resta il default) oppure **OpenStreetMap** (Leaflet 1.9.4 incluso nel modulo, nessuna chiave né account, nessuna CDN).
- Il JavaScript usa un motore per provider con la stessa interfaccia; "Indicazioni stradali" apre Google Maps o openstreetmap.org a seconda del provider.
- `Helper\Data::getMapConfig()` / `isMapAvailable()`: configurazione mappa condivisa con `m2-store-pickup`.
- Whitelist CSP per `tile.openstreetmap.org`; traduzione italiana.

## 1.1.1 — 2026-10-14
- Admin: il tab con indirizzo e coordinate si chiama "Indirizzo" (prima veniva tradotto "Negozio").

## 1.1.0 — 2026-10-14
- Elenco negozi lato server: solo negozi **attivi** e assegnati alla **store view** corrente, ordinati per "Ordinamento" e nome.
- In elenco e nel fumetto della mappa: descrizione, indirizzo, telefoni, email, sito, social, **orari di apertura** e link "Indicazioni stradali".
- **Vicino a me**: ordina i negozi per distanza dalla posizione del cliente (calcolo nel browser, nessuna API in più).
- Ricerca per città, CAP, indirizzo o nome che filtra elenco e mappa.
- **Map ID** configurabile: con Map ID la mappa usa gli Advanced Marker, senza usa i marker classici (prima il Map ID era scritto nel codice).
- JavaScript senza jQuery né RequireJS: funziona con Luma, Breeze e Hyvä; Google Maps caricato solo quando la mappa è visibile.
- Titolo pagina, meta title/description/keywords, zoom e blocchi CMS prima/dopo la mappa ora vengono applicati (il percorso dei blocchi CMS era errato).
- Admin: etichette tradotte, orari di apertura salvati, solo i campi previsti vengono salvati, coordinate validate, permessi ACL corretti, voce "Impostazioni" nel menu.
- Schema del database dichiarativo (`db_schema.xml`): aggiunge le colonne `sort_order` e `open_hours` alle installazioni esistenti.
- Whitelist CSP per Google Maps; rimosso Font Awesome da CDN; traduzione italiana completa.

## 1.0.3 — 2026-10-06
- Vincolo PHP allineato agli altri moduli (`^8.1`).

## 1.0.2
- Correzioni minori.

## 1.0.1
- Correzioni minori.

## 1.0.0
- Prima versione: pagina store locator con mappa Google e gestione negozi da admin.
