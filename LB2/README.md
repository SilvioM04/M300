LB2 Dokumentation
==========================================================

### Inhaltsverzeichnis
- Einführung
- Vagrantfile
- Testing
- Quellen

### Einführung

Da viele Leute einen Webserver mit einer Datenbank erstellen, wollten wir etwas "Besondereres" machen. Der Apache2-Webserver läuft im Frontend, daher sollten die Admin- und OPcache-Dienste in der GUI sichtbar sein. PHP und MariaDB werden im Hintergrund ausgeführt, damit die Dienste ordnungsgemäß ausgeführt werden. Auf all dies sollte über die Portweiterleitung zugegriffen werden.

Hierzu hatte ich noch einen Netzwerkplan erstellt.
![Virtualbox installed](../Bilder/Netzwerkplan.png)

Auf dem Hostsystem können wir http://localhost:2123 eingeben. Anschliessend leitet dieser die Anfrage an die VM auf Port 80 weiter. Wir sollten in der Lage sein, die Services so nutzen zu können.

Damit ich die VM per Vagrant erstellen konnte braucht man zwingend diese zwei Befehle:
```
$ vagrant init generic/ubuntu1804 # Vagrantfile wird mit der Box Ubuntu 18.04 erstellt
$ vagrant up # Die Virtuelle Maschine wird gestartet
```

Damit man nicht die ganze Zeit das Vagrantfile anpassen muss kann man auch mit diesem Befehl auf die VM zugreifen:
´´´
$ vagrant ssh 
´´´

Es gibt aber noch weiter Befehle die man kennen muss wie zum Beispiel diese hier:
´´´
$ vagrant halt # VM ausschalten
$ vagrant status # Status der VM wird angezeigt
$ vagrant destroy # Die VM wird endgültig gelöscht
´´´






### Wissenstand

Mit Git, einem verteilten Versionskontrollsystem, ist die Code-Zusammenarbeit und Änderungsverfolgung möglich. Dieses Tool ist besonders nützlich, wenn Sie an großen Projekten arbeiten oder Code-Updates verwalten. 

Die Verwaltung virtueller Entwicklungsumgebungen ist einfach mit Vagrant, einem Tool, das die Erstellung virtueller Maschinen und die Installation der erforderlichen Software automatisiert. Es wurde entwickelt, um Entwicklern dabei zu helfen, ihre Umgebung an bestimmte Anforderungen anzupassen, z B. Software und Betriebssystem benötigt, um dies zu ermöglichen. 

Anwendungen und Netzwerke können durch Implementierung eines Reverse-Proxys oder einer Firewall geschützt werden. Firewalls sollen unerwünschten Datenverkehr blockieren, während ein Reverse-Proxy-Server ein Vermittler zwischen Client- und Serverprogrammen ist. Es ist wichtig, dass beide Mechanismen zum Schutz vor feindlichen Aktivitäten wie Cyberangriffen funktionieren. 

Die Verwendung von Code zum Erstellen und Verwalten von Infrastrukturkomponenten wie Servern, Netzwerken und Datenbanken wird als IaC (Infrastructure as Code) bezeichnet. IaC ist ein innovativer Ansatz zur Automatisierung des Infrastrukturmanagements, der es Entwicklern und IT-Teams ermöglicht, Infrastrukturen schneller und effizienter bereitzustellen und zu verwalten.

IT-Ressourcen und -Dienste, die über das Internet bereitgestellt werden, sind das Herzstück von Cloud Computing. Es wird von einem Drittanbieter betrieben und umfasst Infrastruktur, Software und Plattformen. Dank Cloud Computing müssen Unternehmen keine eigene Infrastruktur aufbauen, was es zur idealen Lösung für diejenigen macht, die eine flexible und skalierbare IT-Infrastruktur suchen.

Um den Zugriff auf vertrauliche Daten und Systeme zu kontrollieren, ist es wichtig, über Mechanismen zu verfügen, um die Identität und die Berechtigungsstufe von Benutzern im Computersystem oder in der Anwendung zu überprüfen. Die beiden Hauptmechanismen sind Authentifizierung und Autorisierung. Die Authentifizierung verifiziert die bestätigte Identität eines Benutzers und stellt sicher, dass er der ist, der er ist, während die Autorisierung definiert, welche Aufgaben er nach der Verifizierung ausführen kann. Nur autorisierte Benutzer haben Zugriff auf die sensiblen Daten und Systeme, die diese Mechanismen effektiv schützen.

In einem Computersystem oder einer Anwendung ist die Benutzerkontenverwaltung als Benutzerverwaltung bekannt, die das Erstellen, Ändern und Löschen von Benutzerkonten bei gleichzeitiger Gewährung des Zugriffs beinhaltet. Es ist äußerst wichtig, Benutzerkonten zu kontrollieren, damit nur autorisierte Benutzer Zugriff auf das System haben.

Secure Shell (SSH) ist ein Protokoll, das verwendet wird, um sich sicher mit einem entfernten Computer oder Server zu verbinden. Dieser Mechanismus gewährleistet sichere Dateiübertragungen und ermöglicht es Benutzern, Befehle auszuführen. SSH ist ein wichtiges Sicherheitstool für die Verwaltung Ihres Netzwerks und Ihrer Server.



