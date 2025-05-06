# Introduction and Goals

## Requirements Overview

### Yappi Companion Apps

**CA-FR-01 Platform Integration:**

- Requirement: Das System MUSS sich nahtlos in bestehende Entwicklerworkflows
  integrieren lassen und dabei die Yappi-Plattform erweitern.
- Priority: High
- Type: Functional
- Source: TBD

**CA-FR-02 Minimal Interrupt:**

- Requirement: Die Companion Apps MÜSSEN die Entwicklerzufriedenheit messen
  können, ohne den Arbeitsfluss zu unterbrechen.
- Priority: High
- Type: Functional
- Source: TBD

**CA-FR-03 Sign On:**

- Requirement: Die Companion Apps MÜSSEN sich über einen einmalig generierten
  Token gegenüber der Yappi-Plattform authentifizieren und autorisieren, um
  Zufriedenheitsdaten erfassen zu können. Der Token MUSS in der Companion App
  gespeichert werden.
- Priority: Medium
- Type: Functional
- Source: TBD

**CA-FR-04 Adding Optional Free Text:**

- Requirement: Die Companion Apps müssen ein optionales Freitextfeld für kurze
  Anmerkungen zur verfügung stellen.
- Priority: Low
- Type: Functional
- Source: TBD

> [!Note]
>
> Das Freitexfeld erhält eine niedrige Priorität, da diese Art von Daten nicht
> automatisch ausgewertet werden können und damit nicht sichergestellt ist, dass
> diese Daten überhaupt nützlich sind.

### IntelliJ IDEA Companion

**IJC-FR-01 Plugin installation:**

- Requirement: Die Companion App MUSS als IntelliJ Plugin installiert und über
  die IDE Settings aktiviert werden können.
- Priority: High
- Type: Functional
- Source: TBD

**IJC-FR-02 Post Commit:**

- Requirement: Das Plugin MUSS den Benutzer nach einem Commit automatisch dazu
  auffordern Zufriedenheitsdaten zu erfassen.
- Priority: High
- Type: Functional
- Source: TBD

**IJC-FR-03 Context Aware Feedback:**

- Requirement: Das Plugin MUSS kontextbasierte Zufriedenheitserfassungen
  ermöglichen. Dazu muss die Zufriedenheit und Kontextdaten zum dazugehörigen
  Commit erfasst werden.
- Priority: Medium
- Type: Functional
- Source: TBD

### Outlook Companion

**OLC-FR-01 Add-In Installation:**

- Requirement: Die Companion App MUSS als Outlook Add-In installiert und über
  die Outlook-Einstellungen aktiviert werden können.
- Priority: High
- Type: Functional
- Source: TBD

**OLC-FR-02 Post Meeting:**

- Requirement: Das Add-In MUSS den Benutzer nach jedem Meeting mit mindestens 2
  Teilnehmern automatisch dazu auffordern Zufriedenheitsdaten zu erfassen.
  Zusätzlich zur geplanten Meetingdauer soll auch die Effektive Meetingdauer
  erfasst werden können.
- Priority: High
- Type: Functional
- Source: TBD

**OLC-FR-03 Context Aware Feedback:**

- Requirement: Das Add-In MUSS kontextbasierte Zufriedenheitserfassungen
  ermöglichen. Dazu müssen die Zufriedenheit und Kontextdaten zum dazugehörigen
  Meeting erfasst werden.
- Priority: Medium
- Type: Functional
- Source: TBD
