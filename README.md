[README.md](https://github.com/user-attachments/files/32183772/README.md)
# OoT Sammel-Checklisten – Nobara Edition

Eine lokale Linux-Checkliste für **The Legend of Zelda: Ocarina of Time** mit Fokus auf **Nobara Linux**. Die App läuft lokal auf deinem Rechner, öffnet die Oberfläche im Browser und speichert den Fortschritt als lokale Datei.

> **Version:** 2.7.0  
> **Status:** in Entwicklung / Community-Projekt  
> **Inoffiziell:** Dieses Projekt steht nicht in Verbindung mit Nintendo, Zelda Chronicles, Zelda Europe oder dem Nobara Project.

## Funktionen

- 224 separat abhakbare Sammel-/Fortschrittseinträge
- 36 Herzteile
- 100 Goldene Skulltulas
- 11 Schritte des Tauschgeschäfts
- 8 Masken
- 10 Nachtschwärmer
- 10 Feen & Feenquellen
- 10 Wundererbsen
- 4 Flaschen
- 12 Ocarina-Lieder
- 23 Ausrüstungsgegenstände & Upgrades
- Fundort, verständliche Beschreibung und Voraussetzungen pro Eintrag
- Alter/Voraussetzungen wie Kind, Erwachsener, Nacht, Item, Lied oder Quest-Fortschritt
- Suche, Filter, Notizen und Fortschrittsanzeige
- lokale Speicherung ohne Online-Konto
- Import/Export von Sicherungen
- Bildergalerien mit optionalem lokalem Nachladen
- Nobara/KDE-freundlicher Starter und Desktop-Eintrag
- keine Python-Pakete via `pip` notwendig

## Schnellstart auf Nobara

### Empfohlen: Installer

Lade den Release-Installer herunter und führe ihn **ohne `sudo`** aus:

```bash
cd ~/Downloads
sh OoT-Nobara-Installieren-v2.7.run
```

Zum Aktualisieren einer laufenden älteren Version:

```bash
sh OoT-Nobara-Installieren-v2.7.run --restart
```

### Direkt aus dem Repository

```bash
git clone <DEINE-GITHUB-REPO-URL>
cd oot-checkliste-nobara
sh NOBARA-INSTALLIEREN.sh
```

Nur lokal starten, ohne Installation:

```bash
sh STARTEN.sh
```

Ohne Online-Nachladen starten:

```bash
sh STARTEN.sh --no-download
```

## Voraussetzungen

- Linux; optimiert für Nobara Linux
- Python 3.8 oder neuer
- aktueller Browser
- für automatische Browseröffnung: `xdg-utils`

Auf Nobara/Fedora bei Bedarf:

```bash
sudo dnf install python3 xdg-utils
```

Die App selbst wird **nicht mit `sudo`** gestartet oder installiert.

## Speicherung

Der Fortschritt liegt standardmäßig hier:

```text
~/.local/share/oot-herzteil-checkliste/fortschritt-v2.json
```

Programmdateien bei einer Benutzerinstallation:

```text
~/.local/share/oot-herzteil-checkliste-programm/
```

Startprotokoll:

```text
~/.local/state/oot-checklisten/letzter-start.log
```

## Diagnose

```bash
sh DIAGNOSE.sh
```

Oder über das App-Menü bzw. in der App unter **Sichern & verwalten**.

## Tests

Die Tests verwenden nur die Python-Standardbibliothek:

```bash
python3 -m unittest discover -s tests -v
```

## Projektstruktur

```text
oot-checkliste-nobara/
├── app.py                 # lokaler HTTP-Server / API
├── launcher.py            # robuster Bootstrap
├── desktop_support.py     # Nobara/Desktop-Integration
├── guide_reader.py        # Guide-/Bild-Nachladen
├── catalog.json           # Checklisten-Daten
├── index.html             # Hauptoberfläche
├── ui.js                  # UI-Logik
├── nobara-ui.js           # Nobara-spezifische UI-Ergänzungen
├── style.css              # Design
├── STARTEN.sh             # lokaler Start
├── INSTALLIEREN.sh        # Benutzerinstallation
├── NOBARA-INSTALLIEREN.sh # Installieren + starten
├── DIAGNOSE.sh            # Diagnose
├── STOPPEN.sh             # lokalen Server beenden
├── tests/                 # automatisierte Tests
├── .github/workflows/     # GitHub Actions
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
└── NOTICE.md
```

## Quellen & Inhalte

Die Checklistenstruktur basiert auf den im Projekt dokumentierten Ocarina-of-Time-Guides. Die verwendeten Quellen stehen in [`QUELLEN.txt`](QUELLEN.txt).

Die Anwendung enthält **keine eingebetteten Originalbilder aus den Guides**. Bildadressen können von der App optional lokal abgerufen werden. Externe Inhalte bleiben Eigentum der jeweiligen Rechteinhaber.

Die detaillierten Fundort- und Voraussetzungstexte wurden in mehreren Kategorien anhand vom Projektbetreiber bereitgestellter Zelda-Europe-Guides überarbeitet. Vor einer öffentlichen Weiterverbreitung sollte geprüft werden, ob die jeweilige Nutzung der Guide-Inhalte und -Formulierungen durch die Rechteinhaber erlaubt ist. Siehe [`NOTICE.md`](NOTICE.md).

## Lizenz

Der **Programmcode und die originale Benutzeroberfläche** stehen unter der MIT-Lizenz. Externe Zelda-/Guide-Inhalte sind ausdrücklich **nicht** Bestandteil dieser Lizenz. Siehe [`LICENSE`](LICENSE) und [`NOTICE.md`](NOTICE.md).

## Fehler melden

Bitte bei einem Fehler möglichst angeben:

- Nobara-Version / Desktop (KDE oder GNOME)
- Python-Version (`python3 --version`)
- was du angeklickt hast
- genaue Fehlermeldung
- optional die erzeugte Diagnose-Datei

Keine privaten Notizen oder Spielstanddateien veröffentlichen, wenn du sie nicht teilen möchtest.

## ⚠️ Disclaimer / Rechtlicher Hinweis / Haftungsausschluss

Dieses Projekt ist ein **inoffizielles, nichtkommerzielles Fanprojekt** für *The Legend of Zelda: Ocarina of Time*.

Es besteht **keine Verbindung, Partnerschaft, Unterstützung oder offizielle Zusammenarbeit mit Nintendo** oder anderen Rechteinhabern der *The Legend of Zelda*-Reihe.

**The Legend of Zelda**, **Ocarina of Time**, Nintendo sowie sämtliche dazugehörigen Namen, Charaktere, Logos, Grafiken, Musikstücke, Spielinhalte und Marken sind Eigentum ihrer jeweiligen Rechteinhaber.

Dieses Projekt dient ausschließlich als persönliche Sammel- und Fortschritts-Checkliste für Spieler.

### Inhalte und Quellen

Einige Informationen zu Fundorten, Voraussetzungen, Sammelobjekten und Spielinhalten basieren auf öffentlich verfügbaren Guides, Informationsseiten und weiteren Quellen rund um *The Legend of Zelda: Ocarina of Time*.

Texte, Bilder, Screenshots, Logos, Namen oder sonstige Inhalte Dritter bleiben Eigentum der jeweiligen Urheber und Rechteinhaber.

Die im Repository enthaltene Software-Lizenz gilt ausschließlich für den **selbst erstellten Programmcode und die dazugehörigen Projektdateien**, soweit diese nicht auf Inhalten Dritter beruhen.

Eine Software-Lizenz wie beispielsweise die MIT License überträgt **keine Rechte an Nintendo-Marken, Zelda-Inhalten, Bildern, Texten oder sonstigem urheberrechtlich geschützten Material Dritter**.

Sollten Rechteinhaber der Auffassung sein, dass bestimmte Inhalte entfernt, geändert oder ersetzt werden müssen, können entsprechende Inhalte aus dem Projekt entfernt oder angepasst werden.

### Keine kommerzielle Nutzung

Dieses Projekt wurde als kostenloses Fanprojekt erstellt.

Es ist nicht dafür vorgesehen, Nintendo-, Zelda- oder andere geschützte Inhalte kommerziell zu verkaufen, zu lizenzieren oder anderweitig gewinnorientiert zu verwerten.

### Haftungsausschluss

Diese Software wird **ohne Gewähr** und **auf eigene Verantwortung** verwendet.

Der Autor übernimmt, soweit gesetzlich zulässig, **keine Haftung für Schäden, Verluste oder sonstige Nachteile**, die direkt oder indirekt durch die Nutzung, Installation, Aktualisierung, Deinstallation oder Fehlfunktion dieser Anwendung entstehen.

Dies betrifft insbesondere, aber nicht ausschließlich:

- Datenverlust
- beschädigte oder gelöschte Dateien
- Verlust von Spielständen
- Verlust von Notizen oder Einstellungen
- Verlust von Backups oder Exportdateien
- Fehlfunktionen des Betriebssystems
- Probleme mit Windows, Linux oder Nobara
- Probleme mit Python, Browsern oder anderen benötigten Programmen
- beschädigte oder veränderte Konfigurationen
- fehlgeschlagene Installationen
- fehlgeschlagene Updates
- fehlgeschlagene Deinstallationen
- Software-Abstürze
- Systemabstürze
- Inkompatibilitäten mit anderer Software
- Probleme durch Sicherheitssoftware, Firewalls oder Antivirenprogramme
- nicht erreichbare externe Webseiten, Bilder oder Informationsquellen
- beschädigte oder nicht mehr lesbare lokale Fortschrittsdateien
- sonstige direkte oder indirekte Schäden

Die Software wird in dem Zustand bereitgestellt, in dem sie veröffentlicht wurde (**"as is"**).

Es wird keine ausdrückliche oder stillschweigende Garantie dafür übernommen, dass:

- die Anwendung fehlerfrei funktioniert,
- die Anwendung auf jedem System funktioniert,
- alle Inhalte vollständig oder korrekt sind,
- alle Fundorte oder Voraussetzungen fehlerfrei angegeben sind,
- alle Daten dauerhaft gespeichert bleiben,
- externe Bilder oder Quellen dauerhaft verfügbar sind,
- die Anwendung für einen bestimmten Zweck geeignet ist.

Die Nutzung erfolgt freiwillig und auf eigenes Risiko.

### Datensicherung

Es wird ausdrücklich empfohlen, vor:

- Installation,
- Update,
- Deinstallation,
- Änderungen an den Programmdateien,
- größeren Änderungen am Betriebssystem

wichtige Daten zu sichern.

Zusätzlich sollte regelmäßig die integrierte Backup-/Export-Funktion verwendet werden, um Fortschritt, Häkchen und Notizen zu sichern.

Der Autor kann nicht garantieren, dass lokale Daten unter allen Umständen erhalten bleiben.

### Schäden an Hard- oder Software

Soweit gesetzlich zulässig, übernimmt der Autor insbesondere **keine Haftung für Schäden an Hard- oder Software**, die durch:

- fehlerhafte Bedienung,
- inkompatible Systeme,
- externe Programme,
- beschädigte Dateien,
- veränderte Systemkonfigurationen,
- manuelle Änderungen am Programm,
- Sicherheitssoftware,
- Betriebssystem-Updates
- oder andere technische Umstände

entstehen.

### Nutzung auf eigenes Risiko

Mit der Nutzung dieser Software akzeptiert der Nutzer, dass er die Anwendung **auf eigenes Risiko** verwendet.

Der Autor ist nicht verantwortlich für Schäden, Datenverlust, Fehlfunktionen oder andere Probleme, die durch die Nutzung oder Veränderung dieser Software entstehen können.

Zwingende gesetzliche Haftungsansprüche, die nach geltendem Recht nicht ausgeschlossen werden dürfen, bleiben hiervon unberührt.

---

> **Kurz gesagt:**  
> Dieses Projekt ist ein inoffizielles Fanprojekt und steht in keiner Verbindung zu Nintendo.  
> *The Legend of Zelda*, *Ocarina of Time* und alle zugehörigen Marken und Inhalte gehören den jeweiligen Rechteinhabern.  
> Die Nutzung der Software erfolgt auf eigene Verantwortung. Für Datenverlust, Schäden oder Fehlfunktionen wird, soweit gesetzlich zulässig, keine Haftung übernommen.
