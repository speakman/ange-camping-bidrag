# Ånge Camping · Bidragsläget

Statisk webbsida som visar bidragslandskapet för Ånge Camping ideell förening:
aktuella spår, deadlines, belopp, krav och källor med konfidens.

**Live:** https://speakman.github.io/ange-camping-bidrag/

## Innehåll

- `docs/index.html` — sidan (single-file, vanilla HTML/CSS/JS)
- `docs/data.json` — GENERERAS ur `bidrag/databas.yaml` +
  `bidrag/ansokningar/*/status.yaml` i huvudarbetsytan med
  `python3 tools/bidragssida.py` — rätta aldrig här, ändra i källorna

## Lokalt

    cd docs && python3 -m http.server 8000
