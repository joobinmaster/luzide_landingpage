# Luzide Landingpage: Platzhalter und Pflege

Jede Datei einfach unter genau diesem Namen ablegen. Sie erscheint automatisch, ohne Änderung am Code. Solange sie fehlt, zeigt die Seite eine beschriftete Fläche.

## Bilder (Ordner img)

| Datei | Format | Inhalt | Wo |
|---|---|---|---|
| img/screen_uhr.webp | 1:1, rund | Screenshot Uhr-App. Solange er fehlt, wird der Uhr-Rahmen ausgeblendet | Abschnitte 7 und 8 |
| img/geraete.webp | vorhanden | Handy und Uhr, freigestellt, nur noch Ersatz, falls das Hero-Video nicht lädt | Hero |

## Video und Ton

| Datei | Format | Hinweis |
|---|---|---|
| video/hero.webm und .mp4 | vorhanden, 9:16 | App-Video, startet mit dem Kachelbruch, läuft in Schleife. Eintrag „cosimo“ ist unscharf gestellt |
| video/lauf.webm und .mp4 | vorhanden, 16:9 | Abschnitt 5, spielt einmal |
| video/einschlafen.webm und .mp4 | vorhanden, 16:9 | Abschnitt 2, spielt einmal und bleibt auf dem letzten Bild stehen. Vorschaubild img/einschlafen_start.webp |
| video/spiegel.webm und .mp4 | vorhanden, 9:16 | Abschnitt 4. Bei 1,2 s erscheint der erste Satz, bei 10,2 s der zweite und alle Fugen leuchten auf |
| video/verwandlung.webm und .mp4 | vorhanden, 9:16 | Abschnitt 6, Sekunde 15 bis 25 aus dem Adler-Video, bleibt im Meditationssitz stehen |
| audio/klang.mp3 | kurz, wenige Sekunden | Der Trainingston. Bis dahin spielt die Seite einen weichen Ersatzgong aus dem Browser |

## Formular

In index.html beim Formular `data-endpoint="TALLY_ENDPOINT"` durch die Tally-Adresse ersetzen. Bis dahin zeigt der Knopf einen Hinweis, dass die Anmeldung gerade angebunden wird.

## Neuigkeiten

Neue Beiträge in news.json eintragen, direkt auf GitHub im Browser. Die neuesten drei erscheinen auf der Seite, der Rest hinter „Alle Neuigkeiten“.

```json
{
  "date": "2026-10-19",
  "title": { "de": "Titel auf Deutsch", "en": "Title in English", "es": "Título en español" },
  "text":  { "de": "Kurzer Text.", "en": "Short text.", "es": "Texto breve." },
  "image": "img/news_beta.webp"
}
```

`image` darf `null` sein. Fehlt `es`, zeigt die spanische Seite den englischen Text.

## Knopf-Tests

Test A (Pixel-Schimmer) sitzt auf dem Hero-Knopf, Test B (3D-Knopf) auf dem Absenden-Knopf im Beta-Formular. Nach der Entscheidung wird der gewählte Stil überall eingesetzt.

## Ausgeblendet

Der Abschnitt „Was noch kommt“ ist im Code vorhanden, aber ausgeblendet (SHOW_ROADMAP = False), bis die Zeilen freigegeben sind.

## Noch zu bauen

impressum.html, datenschutz.html, nutzungsbedingungen.html, konto-loeschen.html (Links in der Fußzeile sind schon gesetzt).

## Sprachen

Deutsch steht direkt in index.html, Englisch und Spanisch in den Tabellen EN und ES im Sprachskript. Aufruf mit ?lang=de, ?lang=en oder ?lang=es, sonst nach Browsersprache.

## Domain

Die Datei CNAME enthält luzide.deinlebendeinprojekt.de. Bei Squarespace einen CNAME-Eintrag `luzide` auf `joobinmaster.github.io` setzen.
