# 📥 Installation

[← Zurück zur Übersicht](../README.md)

Family Fables gibt es (noch) nicht im Play Store. Die App wird direkt von dieser Seite installiert.
Das dauert etwa zwei Minuten pro Handy.

## Voraussetzungen

- Android **10 oder neuer**
- Etwa 60 MB freier Speicher
- Für mehrere Handys: am besten alle im **selben WLAN** (zu Hause)

## Schritt für Schritt

1. **Seite öffnen:** Auf dem Handy im Browser die [neueste Version](../../../releases/latest) aufrufen.
2. **APK laden:** Ganz unten bei **Assets** die Datei `familyfables-x.y.z.apk` antippen.
   (Die Datei `update.json` brauchst du nicht, die liest die App selbst.)
3. **Download öffnen:** Benachrichtigung „Download abgeschlossen“ antippen oder die Datei im Ordner *Downloads* öffnen.
4. **Installation erlauben:** Beim ersten Mal fragt Android: *„Aus Sicherheitsgründen ist es nicht erlaubt,
   unbekannte Apps aus dieser Quelle zu installieren.“* → **Einstellungen** → Schalter bei
   *„Dieser Quelle vertrauen“* einschalten → zurück.
5. **Installieren** antippen. Google Play Protect fragt eventuell nach. Dann *„Trotzdem installieren“* wählen.
   Die Warnung kommt, weil die App nicht aus dem Play Store stammt.
6. **Öffnen**, und weiter geht's mit den [ersten Schritten](ERSTE-SCHRITTE.md).

## Updates

Die App sucht selbst nach neuen Versionen. Gibt es eine, erscheint im **Eltern-Bereich** ein Hinweis
mit dem Knopf **„Jetzt aktualisieren“**. Android fragt einmal nach der Erlaubnis, Updates zu installieren.

- Meldet ein anderes Familien-Handy beim Abgleich eine neuere Version, sucht die App sofort selbst nach.
  So bleiben alle Geräte auf demselben Stand.
- Deine Daten (Kinder, Quests, Münzen, Haustiere …) bleiben bei jedem Update erhalten.

### ⚠️ Einmalig von Hand: Wechsel von 0.26.0 oder älter

In Version 0.26.0 und älter bricht das Update in der App mit dieser Meldung ab:

> *Update hat nicht geklappt – Missing android.support.FILE_PROVIDER_PATHS meta-data*

Dann bitte **einmal** die neueste Version wie oben beschrieben von Hand installieren (einfach
„drüber“ installieren, **nicht** vorher deinstallieren). Ab 0.27.0 laufen Updates wieder über die App.

## Probleme bei der Installation

| Meldung | Lösung |
|---|---|
| „App nicht installiert“ / „Paket scheint ungültig zu sein“ | Download war unvollständig: Datei löschen und neu laden |
| „App nicht installiert, da das Paket mit einem bestehenden Paket in Konflikt steht“ | Eine anders signierte Testversion ist installiert. Nur in diesem Fall: vorher ein **Backup** exportieren (Eltern-Bereich → ⚙ → Backup), dann deinstallieren und neu installieren |
| Nichts passiert beim Antippen | In den Android-Einstellungen → Apps → *Browser* → „Unbekannte Apps installieren“ erlauben |
| Play Protect blockiert | „Weitere Details“ → „Trotzdem installieren“ |

Weitere Hilfe: [Hilfe & häufige Fragen](HILFE.md)
