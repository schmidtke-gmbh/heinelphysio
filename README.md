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
an **info@physiotherapie-heinel.de** (Wunsch Susan: zentrale Adresse, auf die auch die Anmeldung Zugriff hat). Netlify erkennt die Formulare automatisch beim nächsten Deploy
(unter "Forms" prüfen, ob beide gelistet sind). Datei-Anhänge (Rezept-Foto, Lebenslauf) werden mitgesendet, max. 8 MB
(Free-Plan: 100 Einsendungen/Monat).

## Vor Livegang (TODO)
1. **Domain:** Überall `https://www.physiotherapie-heinel.de` per Suchen&Ersetzen anpassen, falls andere Domain (Canonical, OG, JSON-LD, sitemap.xml, robots.txt).
2. **E-Mail:** Alle Anfragen und Bewerbungen gehen an `info@physiotherapie-heinel.de` (Netlify-Benachrichtigung). Das Postfach muss unter der Domain existieren, sobald die Domain live ist.
3. **Social Media:** Instagram-Feed (Elfsight) auf index.html einbinden und Instagram-/Facebook-Links im Footer ergänzen, sobald die Profile existieren.
4. **Cookiebot** ist auf allen Seiten eingebunden (ID b1896dae-…, Auto-Blocking). Google Maps ist als „Marketing" markiert und lädt erst nach Einwilligung. In Cookiebot: Domain der Live-Seite eintragen, Scan starten, Banner-Texte auf Deutsch prüfen. Internen Hinweis-Kasten oben in datenschutz.html vor Livegang entfernen.
5. **JobPosting-Schema:** `validThrough` (aktuell 2026-12-31) aktuell halten.
6. **Offene Inhalte von Susan:** Foto Traktionsbehandlung, Video statt Treppenfoto (Eingang), ggf. Bus-/Tram-Linien in der Anfahrt.
