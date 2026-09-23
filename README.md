# Einzeltraining Terminplaner

Eine eigenständige, responsive Web-App zur Planung von Einzeltraining. Die Anwendung verbindet Trainerzeiten, Spieler-Verfügbarkeiten, feste Termine, Trainingsrhythmen, automatische Zeitoptimierung sowie Einnahmen- und Absagestatistiken in einer einzigen HTML-Datei.

## Live-Betrieb mit GitHub Pages

Die Anwendung benötigt keinen Server und keine Installation. Für die Veröffentlichung reicht die Datei `index.html` im Hauptverzeichnis des Repositorys.

1. Neues GitHub-Repository anlegen oder ein vorhandenes Repository öffnen.
2. `index.html` und `README.md` in das Hauptverzeichnis hochladen.
3. Unter **Settings > Pages** als Quelle **Deploy from a branch** auswählen.
4. Branch `main` und Ordner `/ (root)` festlegen.
5. Änderungen speichern und warten, bis GitHub Pages die Seite veröffentlicht hat.

Die Adresse hat anschließend üblicherweise dieses Format:

```text
https://BENUTZERNAME.github.io/REPOSITORYNAME/
```

## Funktionen

### Zeit- und Terminplanung

- Regelmäßige Trainerzeiten nach Wochentag
- Einzelne Trainerzeiten an einem festen Datum
- Standard-Trainingsdauer, voreingestellt auf 60 Minuten
- Manuelle Trainingstermine
- Feste wöchentliche Kindertermine
- Feste Mannschaftstermine als blockierte Zeiträume
- Automatische Planung für die nächsten vier Wochen
- Optimale Nutzung freier Trainerzeiten
- Berücksichtigung bereits belegter und blockierter Zeiträume
- Anzeige des heutigen oder nächsten anstehenden Termins beim Öffnen
- Feststehende Reiterleiste beim Scrollen
- Einheitliche 24-Stunden-Uhrzeit in Fünf-Minuten-Schritten

### Spieler und Trainingswünsche

- Spieler anlegen, bearbeiten und löschen
- Mehrere verfügbare Zeitfenster pro Spieler
- Individueller Preis je Training
- Folgende Trainingsrhythmen:
  - jeden verfügbaren Tag
  - einmal wöchentlich
  - alle zwei Wochen
- Bei einem Zwei-Wochen-Rhythmus Auswahl zwischen geraden und ungeraden Kalenderwochen
- Automatische Berücksichtigung des Rhythmus bei Vorschlägen, Festterminen und Nachrückern

### Automatische Zeitoptimierung

Die Schaltfläche **Zeit optimal planen** wertet folgende Daten gemeinsam aus:

1. verfügbare Trainerzeiten
2. feste Kindertermine
3. Mannschaftstermine und andere blockierte Zeiten
4. Standard-Trainingsdauer
5. Verfügbarkeiten der Spieler
6. gewünschte Trainingshäufigkeit
7. gerade oder ungerade Kalenderwochen
8. bereits erfolgte Einteilungen

Automatisch erzeugte Termine sind in der Wochenplanung als **Optimierter Termin** gekennzeichnet. Manuell angelegte Termine und Festtermine bleiben erhalten.

## Finanzen und Absagen

- Individueller Preis je Spieler
- Preis je Mannschaftstraining
- Geplante Einnahmen der aktuellen Woche
- Getrennte Einnahmen aus Einzel- und Mannschaftstraining
- Einnahmeausfall der aktuellen Woche
- Absagezähler je Spieler
- Gesamtverlust je Spieler
- Gesamter Absageverlauf mit Datum und Uhrzeit
- Nachrückersuche nach einer Absage
- Möglichkeit, eine versehentliche Absagebuchung zu stornieren

Bei einer Absage wird der Spieler aus dem Termin entfernt. Der zugehörige Betrag entfällt aus den geplanten Einnahmen und wird gleichzeitig als Verlust dokumentiert.

## WhatsApp-Ausgabe

Die App erzeugt eine kopier- und teilbare Terminübersicht mit:

- Datum
- Uhrzeit
- Trainingsort
- Schwerpunkt
- eingeteilten Spielern
- freien Plätzen

## Datenspeicherung

Alle Daten werden im lokalen Speicher des verwendeten Browsers gespeichert. Dazu gehören unter anderem:

- Spieler
- Verfügbarkeiten
- Trainingswünsche und Kalenderwochen
- Trainerzeiten
- feste Kindertermine
- Mannschaftstermine
- geplante Termine und Einteilungen
- Preise
- Einnahmen
- Absagen und Verluste
- Wartelisten
- Einstellungen

### Wichtig

Die Daten werden nicht automatisch zwischen verschiedenen Geräten oder Browsern synchronisiert. Firefox, Safari, Chrome und ein als App gespeicherter Startbildschirm können jeweils einen eigenen lokalen Datenbestand haben.

Für den Wechsel auf ein anderes Gerät oder als regelmäßige Sicherung sollte die Export- und Importfunktion verwendet werden.

## Sicherung und Wiederherstellung

Unter **Sicherung** kann der vollständige Datenbestand als JSON-Datei exportiert werden. Der Dateiname enthält Vereinsname, Datum und Uhrzeit.

Zur Wiederherstellung:

1. Reiter **Sicherung** öffnen.
2. **Importieren** auswählen.
3. Zuvor exportierte JSON-Datei auswählen.

## Dateien im Repository

```text
/
├── index.html
├── apple-touch-icon.png
├── icon-512.png
└── README.md
```

`index.html` enthält HTML, CSS und JavaScript vollständig in einer Datei. Weitere Bibliotheken oder Build-Schritte sind nicht erforderlich.

## Bedienung in empfohlener Reihenfolge

1. Unter **Sicherung** Vereinsname, Trainer, Standard-Spielerzahl und Trainingsdauer festlegen.
2. Unter **Meine Zeiten** die regelmäßigen und einzelnen Trainerzeiten erfassen.
3. Unter **Feste Termine** Mannschaftstermine und feste Kindertermine eintragen.
4. Unter **Spieler & Zeiten** Spieler, Preise, freie Zeiten und Trainingswünsche erfassen.
5. **Zeit optimal planen** ausführen.
6. Wochenplanung kontrollieren und bei Bedarf manuell anpassen.
7. WhatsApp-Ausgabe kopieren oder teilen.
8. Daten regelmäßig exportieren.

## Browser und Geräte

Die App ist für Desktop, Tablet und Smartphone optimiert. Die Uhrzeiten werden unabhängig von der Browsersprache im 24-Stunden-Format dargestellt.

Wenn nach einem Update noch eine alte Version erscheint:

- Seite vollständig neu laden
- Browser-Cache leeren
- bei GitHub Pages kurz warten und erneut laden
- eine vorhandene Startbildschirm-Verknüpfung schließen und neu öffnen

## Datenschutz

Die Anwendung überträgt von sich aus keine Daten an einen externen Server. Sämtliche eingegebenen Daten verbleiben im lokalen Browser-Speicher und in den vom Benutzer erstellten Exportdateien.

Da Namen, Telefonnummern und Terminangaben personenbezogene Daten sein können, sollten Repository und Exportdateien entsprechend geschützt werden. Reale Spieler- oder Kontaktdaten sollten nicht direkt in den öffentlich sichtbaren Quelltext eingetragen werden.

## Version

Aktueller Stand: **V10**

Enthalten sind insbesondere:

- Zeitoptimierung
- Festtermine mit Trainingsrhythmus
- gerade und ungerade Kalenderwochen
- Finanzen und Absagestatistik
- heutiger beziehungsweise nächster Termin beim Start
- feststehende Navigation
- einheitliches 24-Stunden-Zeitformat

## Lizenz

Private Nutzung und Anpassung für die eigene Trainingsorganisation. Für eine öffentliche oder gewerbliche Weitergabe sollte eine passende Lizenzdatei ergänzt werden.


## iPhone-Homescreen-Icon

Die Datei `apple-touch-icon.png` wird auf dem iPhone automatisch verwendet, wenn die Website in Safari über **Teilen > Zum Home-Bildschirm** hinzugefügt wird. Alle Dateien müssen im Hauptverzeichnis des GitHub-Repositorys liegen.
