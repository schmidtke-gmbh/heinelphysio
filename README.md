# Physiotherapie Susan Heinel – Website

Statische Website (HTML/CSS/JS, keine Build-Tools) für die Praxis für Physiotherapie Susan Heinel, Chemnitz.

## Seiten
- `index.html` – Startseite (Leistungen, Bewertungen, Termin-Anfrage, FAQ)
- `ueber-uns.html` – Über uns (Team, Praxisrundgang)
- `karriere.html` – Karriereseite (Benefits, Weg ins Team, offene Stelle)
- `bewerbung.html` – Blitzbewerbung (Formular)
- `danke.html` – Bestätigungsseite nach Formularversand (noindex)
- `impressum.html`, `datenschutz.html`
- `sitemap.xml` / `robots.txt` – SEO

## Deployment
GitHub-Repo → Netlify (Import from Git), kein Build-Command, Publish-Directory = Root.

## Formulare (Netlify Forms)
Beide Formulare sind für Netlify Forms vorbereitet (`data-netlify="true"`, Honeypot, Datei-Upload):
- `terminanfrage` (index.html) → leitet nach Versand auf `danke.html`
- `blitzbewerbung` (bewerbung.html) → leitet auf `danke.html?typ=bewerbung`

**Einmalig in Netlify einrichten:** Site → Forms → Form notifications → "Email notification" für beide Formulare
an **physiotherapiesusanheinel@web.de**. Netlify erkennt die Formulare automatisch beim nächsten Deploy
(unter "Forms" prüfen, ob beide gelistet sind). Datei-Anhänge (Rezept-Foto, Lebenslauf) werden mitgesendet, max. 8 MB
(Free-Plan: 100 Einsendungen/Monat).

## Vor Livegang (TODO)
1. **Domain:** Überall `https://www.physiotherapie-heinel.de` per Suchen&Ersetzen anpassen, falls andere Domain (Canonical, OG, JSON-LD, sitemap.xml, robots.txt).
2. **E-Mail:** Kontaktadressen auf der Seite (`info@physiotherapie-heinel.de` im Footer/Impressum/JSON-LD, `bewerbung@…` auf karriere.html) mit Susan abstimmen – Formulare gehen an physiotherapiesusanheinel@web.de.
3. **Platzhalter:** Mitarbeiterzitate (karriere.html), Instagram-Feed (Elfsight) ersetzen.
4. **Cookie-Banner:** Cookiebot einbinden; Google-Maps-iframe (index.html) hinter Consent legen.
5. **JobPosting-Schema:** `validThrough` (aktuell 2026-12-31) aktuell halten.
6. **Offene Inhalte von Susan:** Foto Traktionsbehandlung, Video statt Treppenfoto (Eingang), ggf. Bus-/Tram-Linien in der Anfahrt.
