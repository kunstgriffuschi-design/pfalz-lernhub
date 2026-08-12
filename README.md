# Pfalz Digital Lern-Hub

Der zentrale Lern-Hub von Pfalz Digital: eine Kachel-Startseite, hinter der alle
Lernseiten und Anleitungen rund um KI liegen. Gedacht als „Classroom" im eigenen
Look – ohne Monatsgebühr, gehostet über Netlify.

**Live-Adresse:** `pfalz-lernhub.netlify.app` (später ggf. `lernen.pfalzdigital.de`)

## Aufbau

| Datei / Ordner | Zweck |
|---|---|
| `index.html` | Hub-Startseite mit Themen-Rubriken und Kacheln |
| `lernseiten/` | Eine HTML-Datei pro Lernseite (selbst-enthalten, Fonts eingebettet) |
| `assets/fonts.css` | Markenschriften Anton + Hanken Grotesk als Data-URI (DSGVO-sicher, kein Google-Abruf) |
| `media/` | Videos und Bilder, selbst gehostet (kein YouTube-Embed → DSGVO-sicher) |

## Neue Lernseite veröffentlichen

1. Fertige HTML-Datei nach `lernseiten/` legen (Dateiname klein, ohne Umlaute
   und Leerzeichen, z. B. `claude-erste-schritte.html`).
2. In `index.html` eine neue Kachel (`<a class="karte" …>`) ergänzen und die
   passende(n) Rubrik(en) in `data-rubriken` eintragen
   (`ki-videos`, `claude`, `recht`).
3. Beides committen und zu GitHub pushen – Netlify stellt die Seite danach
   automatisch online.

## Startervideo aktivieren

Der Begrüßungsblock ist in `index.html` schon vorbereitet, aber ausgeblendet.
Sobald Jörgs Original-Aufnahme fertig ist: MP4 als
`media/startervideo-joerg.mp4` ablegen, im `<section id="starter">`-Tag das
Wort `hidden` entfernen, committen, pushen. (Genaue Schritte stehen als
Kommentar direkt über dem Block in `index.html`.)

## Regeln

- Schriften niemals live von Google-Servern laden (DSGVO) – entweder
  `assets/fonts.css` einbinden oder als Data-URI einbetten.
- Farben und Schriften: Pfalz-Digital-CI (Navy `#071A37`, Rot `#DF241D`,
  Gold `#E8C66F`, Paper `#F8F4EA`; Anton für Headlines, Hanken Grotesk für Text).
- Die Originale bleiben zusätzlich im OneDrive-Team-Ordner
  „KI Skills für Claude" – dieses Repository ist die veröffentlichte Fassung.
- **Interne Lernseiten gehören nicht hierher:** Alles in diesem Repository ist
  öffentlich erreichbar. Seiten mit Team-Interna (Ablageorte, Konten, IDs,
  Kosten) bleiben ausschließlich im OneDrive-Team-Ordner.
