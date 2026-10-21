# 🔒 Datenschutz in Kurzform

[← Zurück zur Übersicht](../README.md)

> Dies ist eine verständliche Zusammenfassung für Testfamilien, keine vollständige Datenschutzerklärung.
> Die ausführliche, rechtlich geprüfte Fassung folgt zur öffentlichen Veröffentlichung.

**Verantwortlich:** Dominik Zeh · E-Mail: dev@familyfables-app.de

## Das Wichtigste

- ✅ **Kein Konto, keine Werbung, kein Tracking, keine Analyse-Dienste**
- ✅ **Eure Daten bleiben auf euren Geräten.** Es gibt keinen Server, auf dem eure Familie gespeichert wird
- ✅ Fotos werden nur als Aufgaben-Nachweis gemacht, verkleinert gespeichert und mit der Aufgabe gelöscht
- ✅ Die Eltern-PIN wird nur als nicht umkehrbarer Hash gespeichert

## Was wo liegt

| Was | Wo |
|---|---|
| Vornamen/Spitznamen und Alter der Kinder | Nur auf euren Familien-Geräten |
| Aufgaben, Münzen, Haustiere, Story-Fortschritt | Nur auf euren Familien-Geräten |
| Fotos als Aufgaben-Nachweis | Nur auf euren Geräten; nach der Prüfung mit der Aufgabe gelöscht |
| Stimmungs-Check und Förderziele (falls eingeschaltet) | Nur auf euren Familien-Geräten |

## Abgleich zwischen den Handys

- Im **Heim-WLAN** tauschen eure Geräte die Daten direkt untereinander aus. Das geht nur mit dem gemeinsamen
  **Familien-Schlüssel**, den ein Gerät beim Beitritt (QR-Code oder 6-stelliger Code) bekommt.
- **Abgleich unterwegs** *(nur mit eurer Einwilligung, jederzeit widerrufbar)*: Finden sich die Handys nicht im WLAN,
  läuft der Abgleich über Google Firebase (Speicherort Frankfurt am Main). Die Daten werden vorher auf dem Handy
  **Ende-zu-Ende verschlüsselt** (AES-256). Der Dienst sieht nur unlesbaren Datensalat, keine Namen,
  Aufgaben oder Fotos. Fotos werden dort gelöscht, sobald die Aufgabe geprüft ist.

## Einwilligung

Beim Einrichten (und einmalig nach dem Update auf 0.30) stimmt ein Elternteil den Datenschutzhinweisen zu,
bei bestehenden Familien bestätigt mit der Eltern-PIN. Freiwillig und einzeln wählbar, nicht vorausgewählt:

- **Gefühls-Check und Förderziele** (können Gesundheitsdaten sein, deshalb ausdrückliche Einwilligung)
- **Abgleich unterwegs** (Google Firebase)
- **KI-Geschichten** (Google Gemini)

Widerruf jederzeit unter Eltern-Bereich → Einstellungen → **Datenschutz**. Beim Widerruf werden die zugehörigen
Daten gelöscht (Gefühle und Ziele auf allen Geräten, beim Abgleich unterwegs die Familiendaten in Firebase).
Die vollständigen Datenschutzhinweise stehen in der App.

## Was die App ins Internet schickt

- **Update-Prüfung:** Die App fragt bei GitHub nach, ob es eine neue Version gibt. Dabei werden keine Familiendaten gesendet.
- **Optionale KI-Geschichten:** Nur wenn Eltern selbst einen Gemini-Schlüssel hinterlegen. Dann gehen der
  **Aufgabentext und das Alter** an Google, **keine Namen und keine Fotos**.
- Sonst nichts.

## Berechtigungen

| Berechtigung | Wofür |
|---|---|
| Kamera | Foto-Nachweis und QR-Code scannen, nur auf Wunsch |
| WLAN / Netzwerk | Abgleich im Heim-WLAN, Update-Prüfung |
| Benachrichtigungen | Hinweise auf neue Quests, Fotos zum Prüfen, hungrige Haustiere |
| Apps installieren | Damit sich die App selbst aktualisieren kann |
| Akku-Optimierung ignorieren | Damit der Abgleich im Hintergrund nicht ausgebremst wird (nur nach Nachfrage) |

## Löschen

Eltern-Bereich → ⚙ → Familie → **„Alle Inhalte löschen“**, oder die App deinstallieren.
Auf jedem Familien-Gerät einzeln, denn jedes Gerät hat eine eigene Kopie.
