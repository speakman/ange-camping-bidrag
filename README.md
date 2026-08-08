# Ånge Camping · Bidragsläget

Statisk webbsida som visar bidragslandskapet för Ånge Camping ideell förening:
aktuella spår, deadlines, belopp, krav och källor med konfidens.

**Live:** https://speakman.github.io/ange-camping-bidrag/

## Innehåll

- `docs/index.html` — sidan (single-file, vanilla HTML/CSS/JS)
- `docs/data.json` — GENERERAS ur `bidrag/databas.yaml` +
  `bidrag/ansokningar/*/status.yaml` i huvudarbetsytan med
  `python3 tools/bidragssida.py` — rätta aldrig här, ändra i källorna.
  Utfilen är en medveten delmängd: generatorns `PUBLIKA_FALT` avgör vad som
  publiceras.

Sidan bär `noindex` med avsikt: den är publik för den som har länken men ska
inte dyka upp i sökmotorer förrän styrelsen beslutat annat. "Fixa" inte bort
taggen åt något håll utan det beslutet.

## Uppdatera

    # i huvudarbetsytan (monorepot):
    python3 tools/bidragsvakt.py          # databasen ska vara grön
    python3 tools/bidragssida.py          # regenererar docs/data.json
    python3 tools/bidragssida.py --kontroll
    # sedan här: git add docs/ && git commit && git push

## Lokalt

    cd docs && python3 -m http.server 8000
