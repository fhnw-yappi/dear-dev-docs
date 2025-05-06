# Architecture decisions

## AD-001: Keine native Outlook-/Teams-Integration unter macOS
Status: Abgeschlossen / nicht umsetzbar
Kontext:
Unser Add-in soll im Kalender-Lesemodus einen Ribbon-Button bereitstellen (AppointmentOrganizerCommandSurface, VersionOverridesV1_1). Wir sind ausschliesslich macOS-Entwickler und benötigen für die native Integration das Requirement Set 1.8, das Outlook für macOS aktuell nicht vollständig unterstützt.
Entscheidung:
Wir verzichten auf eine native Outlook- oder Teams-Add-in-Integration für macOS. Stattdessen suchen wir nach einer plattform- und client-unabhängigen Alternative (z.B. eine reine Web-App oder Browser-Extension), die auf allen Betriebssystemen gleichermassen funktioniert.
Konsequenzen:
Pro: Kein Blocker durch fehlenden macOS-Support, klare Fokussierung auf eine einheitliche Lösung.
Contra: Verlust der nativen Ribbon-UX, Mehraufwand für Implementierung und Dokumentation einer alternativen Lösung.
Rationale:
Die native API-Unterstützung auf macOS fehlt, und unsere Ressourcen sind auf macOS-Entwicklung beschränkt. Ein Versuch, eine unzuverlässige Ribbon-Integration zu erzwingen, führt zu schlechter Qualität und hohem Wartungsaufwand.

## AD-002: Keine Teams-Add-in-Integration wegen Admin-Freigabe
Status: Offen / In Klärung
Kontext:
Teams-Add-Ins müssen von Firmen- oder Tenant-Administratoren freigeschaltet werden. Diese Abhängigkeit macht unser Produkt yappi für Endnutzer nicht unabhängig einsetzbar.
Entscheidung:
Wir entwickeln kein Teams-Add-in, da die Notwendigkeit einer Admin-Freigabe die Verbreitung und Unabhängigkeit einschränkt. Stattdessen setzen wir auf eine leichter verfügbare Lösung (z.B. ein externes Web-Formular oder automatisierte E-Mail), die ohne zusätzliche Administratorrechte funktioniert.
Konsequenzen:
Pro: Sofortige Verfügbarkeit für alle Nutzer, keine zusätzlichen Admin-Prozesse nötig.
Contra: Keine tiefe Teams-Integration, weniger nahtlose User-Experience innerhalb der Teams-App.
Rationale:
Unabhängigkeit und schnelle Verfügbarkeit haben Vorrang vor tiefgehender, aber behinderter Integration. Externe Web-Lösungen sind einfacher zu rollen und erfordern keine Tenant-Konfiguration.

## AD-003: Einstellung des Web-Add-In-Supports durch Microsoft
Status: Abgeschlossen / nicht mehr verfügbar
Kontext:
Microsoft hat angekündigt, den Support für klassische Web-Add-Ins in bestimmten Umgebungen (z. B. ältere Office-Clients und Teams Desktop) einzustellen und stattdessen auf modernere Ökosysteme zu setzen. Das bedeutet, dass unsere Add-Ins in einigen Szenarien gar nicht mehr ausgeführt werden können.
Entscheidung:
Wir verzichten auf jede Abhängigkeit von Microsoft-Web-Add-Ins und entwickeln stattdessen eine vollständig von Microsoft-Plugins entkoppelte Lösung. Dies kann eine eigenständige Web-App, Browser-Extension oder mobile App sein, die ausserhalb des Office-Ökosystems läuft.
Konsequenzen:
Pro: Keine Bindung an Microsoft-Ökosystem, volle Kontrolle über Auslieferung und Updates, unabhängig von Office-Client-Versionen.
Contra: Verlust direkter Integration (Ribbon-Button, In-Context UI), erhöhter Entwicklungsaufwand für eigene Authentifizierung und UI-Integration.
Rationale:
Da Microsoft den klassischen Web-Add-In-Support zurückzieht, wäre jede Investition in dieses Modell mittelfristig wertlos. Eine eigenständige Lösung sichert Investitionsschutz und ermöglicht uns, die Funktionalität dauerhaft zu betreiben, ohne auf Microsoft-Freigaben oder API-Stabilität angewiesen zu sein.
