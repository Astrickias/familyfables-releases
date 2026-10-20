# Changelog

> **Versionsschema:** Solange die App in der Beta ist, bleibt die Versionsnummer bei 0.x.
> Die früheren Pakete „1.0.0-beta1/2/3“ heißen jetzt 0.13.0, 0.14.0 und 0.15.0. Version 1.0.0 gibt es erst zur Veröffentlichung.

## 0.22.0 – Tägliche Abenteuer (20.10.2026)
- **Neu: Tagesgeschenk 🎁** (Startbildschirm)
  - 7-Tage-Kalender: jeden Tag etwas Neues (Münzen, Leckerlis, EP)
  - Tag 7: **Schatztruhe** mit einem neuen Möbelstück und einem Ei
  - Wer einen Tag auslässt, fängt wieder bei Tag 1 an
- **Haustiere: feste Fütterzeiten** statt 3× beliebig
  - Frühstück (5–12 Uhr), Mittagssnack (12–17 Uhr), Abendessen (17–23 Uhr), nachts schläft das Tier
  - Der Knopf zeigt, ab wann es wieder Hunger hat
- **Neu: Tier-Sammlung mit Eiern 🥚** (Tab „Held“)
  - 9 Tiere in 4 Seltenheiten (Gewöhnlich, Selten, Episch, Legendär), Pyra ist schon dabei
  - Eier gibt es: 1 zum Start, 1 pro 6 erledigte Quests, 1 aus der Schatztruhe, 1 pro Wochen-Herausforderung
  - Ei wackelt, knackt, Tier schlüpft. Neue Tiere werden sofort zum Begleiter, doppelte bringen Bonus-Leckerlis
  - Begleiter jederzeit wechseln
- **Neu: Wochen-Herausforderung 🏆** (Tab „Quests“): 3 Ziele pro Woche, Belohnung 60 Münzen, 40 EP und ein Ei
- **Erinnerungen auf dem Kinder-Handy:** Mahlzeit fürs Haustier (ab 7, 14 und 18 Uhr), Tagesgeschenk (ab 15 Uhr, falls noch nicht abgeholt), neues Ei
- **Für die Testphase:**
  - Eltern → Familie → „Nutzung der letzten 7 Tage“: wie oft und wie lange jedes Kind die App geöffnet hat, dazu das Feedback der Kinder und ein Knopf „Bericht teilen“
  - Kinder können im Tab „Held“ mit einem Tipp sagen, wie ihnen die App gefällt und was sie sich wünschen

## 0.21.0 – Haustiere & Mein Zuhause (20.10.2026)
- **Haustiere neu: Futter sind jetzt Leckerlis 🍖 statt Münzen**
  - Leckerlis gibt es für erledigte Quests (+2) und Story-Folgen (+1), zum Start 3 Stück
  - Füttern höchstens 3× pro Tag
  - Das Haustier wächst über Stufen: Baby → Jungtier → Erwachsen → Legendär (alle 4× Füttern eine Stufe), und wird dabei größer
  - Laune: satt, „hätte gern ein Leckerli“, „hat Hunger!“. Bei Hunger erscheint ein Hinweis auf dem Startbildschirm
  - Animation beim Füttern (Hüpfen + Herz)
- **Neu: Mein Zuhause** (Tab „Held“)
  - Eigenes Zimmer mit 10 Plätzen (Fenster, Wandbild, Regal, Licht, Bett, Hobby-Ecke, Sitzplatz, Pflanze, Boden, Spielzeug)
  - 45 Möbel für 15–160 Münzen, manche erst ab einem bestimmten Level
  - 5 Zimmer-Stile: Schloss, Baumhaus, Kristallhöhle, Unterwasser-Palast, Raumstation
  - Das Haustier spaziert durchs Zimmer
  - Gekauftes steht im Münz-Journal: geht beim WLAN-Abgleich nie verloren und wird nie doppelt bezahlt
- 41 neue 3D-Grafiken (Möbel, Haustier-Launen)
- **Fehler behoben:** Der Update-Hinweis kam nur alle 3 Stunden. Jetzt wird bei jedem Öffnen nachgesehen (höchstens alle 10 Minuten).

## 0.20.0 – Endboss einstellbar (20.10.2026)
- **Familien-Endboss einstellbar** (Eltern → Familie → „Endboss anpassen“):
  - **Wie lange soll der Kampf dauern?** ca. 3 Tage, 1 Woche, 2 Wochen, 1 Monat oder eine eigene Zahl an Lebenspunkten
  - Die App rechnet die Lebenspunkte aus eurem bisherigen Tempo aus (erledigte Aufgaben pro Tag der letzten 2 Wochen, Geschwister-Combos eingerechnet)
  - Eigener **Name**, eigene **Belohnung** („Familien-Pizza-Abend“ …) und Aussehen des Bosses
  - Wahlweise **neuen Kampf starten** (volle Lebenspunkte) oder den bisherigen Schaden behalten
  - Die Karte zeigt: verbleibende Lebenspunkte, voraussichtliche Restdauer und wie oft der Boss schon besiegt wurde
  - Die Kinder sehen am Boss das Ziel, z. B. „Ziel: ca. 1 Woche“
- Einstellungen → „App-Version & Updates“: Link „Alle Änderungen ansehen“

## 0.19.1 – Bugfix (20.10.2026)
- **Absturz beim Start behoben**: 0.19.0 ging sofort wieder zu. Vermutete Ursache ist die Verkleinerung der Release-Version (R8). Sie ist vorerst ausgeschaltet, dadurch verhält sich die Release-Version genau wie die getestete. Die App ist dadurch größer (ca. 60 MB).
- **Absturzmeldung**: Stürzt die App ab, zeigt sie beim nächsten Öffnen einen Fehlerbericht mit „Kopieren“, „Teilen“ und „App neu starten“. Sie sucht dabei gleich nach einer reparierten Version.
- Neuer **Starttest** bei GitHub (Robolectric). Vorerst pausiert, weil die Testumgebung mit den Endlos-Animationen der App nicht zurechtkommt.
- Fehler behoben: Fotos konnten über WLAN nicht übertragen werden (falscher Context in den Server-Routen)
- Fehler behoben: Story-Inhalte wurden nicht geladen (Kommentar-Fehler in StoryContent)

## 0.19.0 – Automatische Updates & Versionsschema (20.10.2026)
- **Automatische Updates auf alle Handys** (Einrichtung: `DEPLOYMENT.md`):
  - GitHub Actions baut bei jedem Versions-Tag eine signierte APK und veröffentlicht sie zusammen mit `update.json`
  - Die App prüft beim Öffnen und alle paar Stunden im Hintergrund: „Update verfügbar“ mit Änderungsliste → **Jetzt aktualisieren** → Android-Dialog bestätigen, die Daten bleiben erhalten
  - Download mit SHA-256-Prüfung, nur über HTTPS. Android akzeptiert nur Updates mit demselben Signatur-Schlüssel
  - Eltern → Zahnrad → **App-Version & Updates**: installierte Version, „Nach Updates suchen“
  - Benachrichtigung „Family Fables x.y.z ist da“ (eigener Kanal „App-Updates“)
- **Versionsschema** nach festen Regeln, eine einzige Stelle: `version.properties`
  - Bugfix → `python3 tools/release/release.py fix "…"` (0.19.0 → 0.19.1)
  - Neue Funktion → `python3 tools/release/release.py feature` (0.19.3 → 0.20.0)
  - versionCode wird berechnet (MAJOR·10000 + MINOR·100 + PATCH)
- Builds aus Android Studio werden mit demselben Schlüssel signiert (sobald `keystore.properties` existiert) und lassen sich ohne Deinstallation über die GitHub-Version installieren
- GitHub Actions prüft außerdem bei jedem Push, ob die App baut und die Tests grün sind

## 0.18.0 – Automatischer Abgleich & Kinder-Handy ohne PIN (Oktober 2026)
- **Fehler behoben: Fotos vom Kinder-Handy kamen nicht beim Eltern-Handy an.** Der WLAN-Abgleich lief bisher nur per Knopfdruck im Eltern-Bereich, und nur ein Gerät kannte den Code des anderen.
  - Neu: Beim ersten Verbinden tauschen die Geräte einen gemeinsamen **Familien-Schlüssel** aus. Danach kennen sich die Geräte gegenseitig.
  - **Automatischer Abgleich**, solange die App offen ist: etwa 1,5 s nach jeder Änderung (Foto abgeschickt, Quest freigegeben …), sobald ein verbundenes Gerät im WLAN auftaucht, und alle 45 s
  - Das Eltern-Handy merkt sich die aktuelle Adresse des Kinder-Handys bei jedem Kontakt (auch nach IP-Wechsel)
  - Eindeutige Gerätenamen (Modell + Kennung): zwei gleiche Handy-Modelle kommen sich nicht mehr in die Quere
- **Kinder-Handy einrichten ohne PIN:** Auf dem Startbildschirm gibt es neu „Kinder-Handy mit Eltern verbinden“:
  Eltern-Handy aus der Liste wählen (oder IP-Adresse eingeben), 6-stelligen Code vom Eltern-Handy eingeben, Kind auswählen, fertig.
  Die Eltern-PIN wird vom Eltern-Handy übernommen.
- **Eltern:** Karte „Geräte verbinden“ (Zahnrad) mit großem Code, IP-Adresse, Liste der verbundenen Geräte und „Jetzt abgleichen“.
  Im Tab „Heute“ zeigt oben eine Zeile „Mit 1 Gerät verbunden · abgeglichen vor 2 Min.“
- **Kind:** Bei eingereichten Fotos steht „Bei deinen Eltern angekommen“ oder „Wird gesendet, sobald das Eltern-Handy die App offen hat“.
- Hinweis: Der Abgleich läuft über das WLAN zu Hause. Damit etwas ankommt, müssen **beide Apps gleichzeitig geöffnet** sein.

## 0.17.0 – Eigene Kamera in der App (Oktober 2026)
- **Fehler behoben: „Kamera konnte nicht geöffnet werden.“** Fotobeweise laufen nicht mehr über die Kamera-App des Geräts, sondern über eine eigene Kamera in Family Fables (Google CameraX).
  - Vollbild-Vorschau, großer goldener Auslöser, Wechsel zwischen Front- und Rückkamera, Blitz-Effekt beim Auslösen
  - Oben steht das Missionsziel, damit das Kind weiß, was aufs Foto gehört
  - Kein Wechsel in eine fremde App mehr: Android kann Family Fables während der Aufnahme nicht beenden, und es gibt keine Galerie-Hintertür in der Kamera-App
  - Fehler werden im Logcat unter `FamilyFablesCamera` protokolliert, mit „Nochmal versuchen“ direkt in der Kamera
- Neue Abhängigkeit: `androidx.camera` 1.4.2 (core, camera2, lifecycle, view)

## 0.16.0 – Fotobeweis repariert, nur noch Kamera (Oktober 2026)
- **Fehler behoben: Fotos gingen verloren.** Zwei Ursachen:
  1. Wurde die App von Android beendet, während die Kamera offen war (auf vielen Handys normal), löschte die App beim Neustart alle Fotos ohne Quest, also auch die frische Aufnahme. Neu: Fotos der letzten 24 Stunden bleiben immer erhalten.
  2. Foto-Dialog und Kamera-Ziel waren nur flüchtig gespeichert. Nach Drehung oder Neustart wurde das Ergebnis verworfen. Neu: Der Zustand wird gesichert, der Dialog öffnet sich wieder und übernimmt die Aufnahme. Notfalls wird sie beim nächsten Öffnen der Quest gerettet.
  - Kamera-Apps, die fälschlich „abgebrochen“ melden, werden erkannt, wenn das Bild trotzdem geschrieben wurde.
  - Klare Meldung, wenn keine Kamera-App vorhanden ist
- **Galerie für Kinder entfernt:** Fotobeweise können nur noch direkt mit der Kamera aufgenommen werden. Alte Bilder lassen sich nicht mehr wiederverwenden.
  Hinweis im Dialog: „Bilder aus der Galerie zählen nicht.“ Nach dem Nachbessern muss ein neues Foto gemacht werden.

## 0.15.0 – UI-Redesign (Oktober 2026)

### Kinder-Seite: Startbildschirm im Spiel-Look
- **Held groß in der Mitte** (3D-Grafik mit Aura in der Heldenfarbe, sanftes Schweben, Partikel), darunter Name und EP-Balken bis zum nächsten Level
- **Eine Hauptaktion:** goldener Knopf „Heutige Quest“ mit Belohnung im Klartext. Er passt sich an: Blitz-Quest, Nachbessern, „Wartet auf Eltern“, „Alles geschafft!“
- **Kompakte Story-Karte** („Neue Folge bereit · Folge 3 von 12“) statt der großen Szenen-Karte
- Kopfzeile nur noch mit Level, Münzen und kleinen Symbolen für Ton, Heldenwechsel und Eltern
- **Bottom-Navigation** mit 4 Bereichen: Abenteuer · Quests · Schatzkammer (Glücksrad, Gutscheine, Ei, Beute) · Held (Haus, Haustier, Battle-Pass, Trophäen, Endboss)
- Entfernt vom Startbildschirm: Weltkarte, Zauber-Rad, Tages-Tipp und Merlin-Begrüßung. Das Glücksrad meldet sich nur noch als kleiner Hinweis, wenn es bereitsteht.
- Sanfte Übergänge zwischen den Bereichen, Klick- und Öffnen-Sounds

### Eltern-Bereich: hell, ruhig, Alltagssprache
- **Eigenes helles Theme** (`ParentTheme`): Dialoge, Schalter und Textfelder sind automatisch hell. Die Systemleisten ziehen mit.
- **3 statt 6 Tabs:** Heute · Aufgaben · Familie
  - **Heute:** Kacheln „Fotos prüfen“ (öffnet direkt das erste Foto) und „Belohnung einlösen“, die Prüf-Liste, „So läuft's heute“ pro Kind mit Fortschritt und dem nächsten offenen Punkt, Knopf „Aufgabe vergeben“
  - **Aufgaben:** Umschalter Aufgaben / Wochenplan / Belohnungen
  - **Familie:** Wochenüberblick, KI-Coach, Urkunden, Chronik
- **Einstellungen hinter dem Zahnrad** (Sprache, Story, Gerät, Kinder, Urlaub, Sync, KI, PIN, Backup, Lizenzen)
- Badge mit der Zahl offener Prüfungen am Tab „Heute“

### Einrichtungsassistent für Eltern
- Erscheint beim ersten Öffnen des Eltern-Bereichs ohne Kinder: So funktioniert's (4 Schritte) → Kind anlegen → erste Aufgabe → Tipps zu Kinder-Gerät und PIN
- Jeder Schritt lässt sich überspringen

### Sonstiges
- 68 neue Texte (DE/EN) in `values*/strings_redesign.xml`
- UI-Test für den Assistenten

## 0.14.0 – Freie Assets (Oktober 2026)
- **166 3D-Symbole** (Microsoft Fluent Emoji, MIT) ersetzen System-Emojis an allen großen Stellen:
  Helden, Haustier, Story-Figuren, Sammelkarten, Belohnungen, Spiele. Einheitlich auf jedem Gerät. Komponente `GameIcon`.
- **Schriften:** Cinzel (Überschriften) und Nunito (Texte), Google Fonts, OFL
- **Echte Sounds statt Piep-Tönen:** Kenney Interface Sounds (CC0) + eigens synthetisierte Spiel-Effekte
  (Münze, Zauber, Stern, Quest bestanden, Level-Up-Fanfare, Wusch). Minispiele haben jetzt Treffer-/Fehler-Sounds.
- Credits & Lizenztexte in der App (Eltern → Familie)
- Neue Ressourcen: ~2 MB (WebP-Grafiken, WAV-Sounds, Schriften). Werkzeuge in `tools/assets/`.

## 0.13.0 – Phase 3 (Oktober 2026)

### Etappe 1 – Architektur & Münz-Journal
- **Münz-Journal**: Münzen und EP werden als unveränderliche Buchungen gespeichert (`LedgerEntry`).
  Der Kontostand ist die Summe aller Buchungen. Deterministische IDs (`quest_<id>`, `spin_<kind>_<tag>`, …)
  sorgen dafür, dass beim WLAN-Sync nichts verloren geht und nichts doppelt zählt. Alte Spielstände werden
  automatisch als Eröffnungsbuchung übernommen.
- `FamilyFablesApplication` + `AppContainer` (eine Instanz von Repository/Sync/Sound pro Prozess)
- `MainViewModel` + Navigation-Compose statt `when(currentArea)` in der Activity
- Unit-Tests: `LedgerTest`, Merge-Logik

### Etappe 2 – Kinder-Tablet-Modus & Benachrichtigungen
- Geräterolle (Eltern → Familie → „Dieses Gerät“): Familien-Gerät, Eltern-Gerät (startet mit PIN),
  Tablet eines Kindes (startet direkt im Dashboard, kein Profilwechsel)
- Lokale Benachrichtigungen: neue Quest, bestanden/nachbessern, Merlin-Nachricht (Kind);
  Foto wartet, Gutschein-Anfrage (Eltern); Fristen-Erinnerung, Tageserinnerung, neue Story-Folge
- WorkManager-Job alle ~15 Min: Routinen, Hintergrund-Sync mit bekannten Geräten, Meldungen
- Unit-Tests: `EventDetectorTest`

### Etappe 3 – Die Chroniken von Eldoria (Story-Kampagne)
- Staffel 1 „Das Erwachen der Sternenquelle“: 12 Folgen, 15 Sammelkarten (3 geheime), 3 Enden
- 6 Minispiele mit Altersanpassung: Rätsel, Memory, Zahlenzauber, Sternenfang, Runen-Folge, Wortzauber
- Entscheidungen beeinflussen spätere Szenen und das Finale
- Tageslimit wie bei einer Serie (Eltern stellen 1–3 Folgen/Tag ein), optional „erst eine Quest“
- Vorlesen (automatisch für unter 6-Jährige), animierte Regionen, Kartenalbum
- Inhalte: `app/src/main/assets/story/season1_<de|en>.json`, erzeugt mit `tools/story/season1_<de|en>.py`
- Unit-Tests: `StoryRulesTest` (inkl. Konsistenzprüfung der echten Staffel-Datei)

### Etappe 4 – Englisch, R8, Barrierefreiheit, UI-Tests
- Komplett zweisprachig (DE/EN, ~650 Texte + Staffel 1). Sprache pro Gerät unter Eltern → Familie → Sprache.
  Texte liegen in `res/values*/strings_*.xml`, Zugriff über `I18n.s(R.string.…)` (funktioniert auch im Repository und Hintergrund).
- Werkzeuge: `tools/i18n/extract_strings.py` (neue Texte extrahieren), `tools/i18n/build_en.py` (EN-Datei bauen & prüfen)
- Release-Build mit R8 (Minify + Resource-Shrinking), Regeln in `src/main/keepRules/rules.keep`
- Screenreader-Beschreibungen für Spielkarten, Runen, Sammelkarten, Symbol-Auswahl
- Compose-UI-Tests: `CoreFlowsUiTest` (PIN-Einrichtung, Rätsel, Glücksrad)

### Neue Abhängigkeiten
- `androidx.work:work-runtime-ktx:2.10.0`
- `androidx.compose.ui:ui-test-junit4` / `ui-test-manifest` (nur Tests)

### Bekannte Punkte zum Testen
- **Release-Build mit R8** einmal auf einem Gerät starten (WLAN-Sync + Story öffnen). Falls etwas abstürzt:
  in `app/build.gradle.kts` `isMinifyEnabled = false` setzen und den Fehler melden.
- Bereits gespeicherte Texte (Verlauf, erstellte Quests) bleiben in der Sprache, in der sie entstanden sind.

## 0.9.0 – Phase 1
Siehe `FEHLERBERICHT_UND_FIXES.md`.
