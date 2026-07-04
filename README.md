# Physiotherapie Susan Heinel – Website

Statische Website (HTML/CSS/JS, keine Build-Tools) für die Praxis für Physiotherapie Susan Heinel, Chemnitz.

## Seiten
- `index.html` – Startseite (Leistungen, Bewertungen, Termin-Anfrage, FAQ)
- `ueber-uns.html` – Über uns (Team, Praxisrundgang)
- `karriere.html` – Karriereseite (Benefits, Weg ins Team, offene Stelle)
- `bewerbung.html` – Blitzbewerbung (Formular)
- `sitemap.xml` / `robots.txt` – SEO

## Deployment (Netlify)
Repo bei GitHub hochladen → Netlify "Import from Git" → kein Build-Command, Publish-Directory = Root.

## Vor Livegang (TODO)
1. **Domain:** Überall `https://www.physiotherapie-heinel.de` per Suchen&Ersetzen anpassen, falls andere Domain gekauft wird (Canonical, OG, JSON-LD, sitemap.xml, robots.txt).
2. **E-Mail:** `info@physiotherapie-heinel.de` / `bewerbung@...` an echte Postfächer anpassen.
3. **Formulare:** Termin- & Bewerbungsformular an Versand anbinden (z. B. Netlify Forms), Demo-Alerts entfernen.
4. **Platzhalter:** Team-Namen, Mitarbeiterzitate (karriere.html), Instagram-Feed (Elfsight) ersetzen.
5. **Cookie-Banner:** Cookiebot einbinden; Google-Maps-iframe (index.html) hinter Consent legen.
6. **JobPosting-Schema:** `validThrough` (aktuell 2026-12-31) aktuell halten.
