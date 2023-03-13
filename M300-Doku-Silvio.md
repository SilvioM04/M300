M300 Dokumentation von Silvio Meier
==========================================================

### Lernziele
Die nachstehende Dokumentation zeigt alle Schritte auf, die es zur Einrichtung einer vollständig funktionsfähigen Toolumgebung benötigt werden.

### Inhaltsverzeichnis
* 01 - Github
* 02 - Git Client
* 03 - VirtualBox
* 04 - Vagrant
* 05 - Packer
* 10 - Fazit

---

01 - Github
======

> [⇧ **Nach oben**](#inhaltsverzeichnis)

Als erstes durften wir einen Github Account erstellen und zudem ein Git Repository erstellen. Die beiden Schritte gingen schnell und unkompliziert.
Ich hatte noch einen SSH-Key erstellt in dem Terminal. Als dieser erstellt wurde konnte ich den SSH-Key im GitHub hinzufügen. Dies hat sehr schnell funktioniert und konnten und dadurch konnte ich mich immer direkt anmelden, da ich einen Privat-Key auf meinem Laptop habe.

---

02 - Git Client
======

> [⇧ **Nach oben**](#inhaltsverzeichnis)

### Was ist Git
Git ist eine weit verbreitete Open-Source-Software zur verteilten Versionskontrolle von Software. Lesen Sie hier, wie das Tool unter Windows funktioniert. Git ist ein Versionskontrollsystem, das vom Linux-Erfinder Linus Torvalds entwickelt wurde.

### Wieso wird Git oft von Programmierern gebraucht?
Einige Vorteile von Git
- Paralleles Arbeiten
- Flexibilität
- Performance
- Einfache Beiträge
- Robustheit
- Gemeinschaft und Freiheit
- etc.

### Die wichtigsten Befehle in Git
**Client Konfigurieren**

Informationen mit Hilfe von Git ändern des GitHub Accounts
``` 
$ git config --global user.name "<username>"
$ git config --global user.email "<e-mail>"
```
**Repository clone/pull**

Clone und Pull eines Reporitorys
```
$ git clone https://gitlab.com/ch-tbz-it/Stud/m300/
$ cd M300  
$ git pull
```
**Repository Push**

Git push wird üblicherweise verwendet, um lokale Änderungen in einem zentralen Repository zu veröffentlichen und hochzuladen. Nachdem Änderungen an einem lokalen Repository vorgenommen wurden, werden die Änderungen per Push für Remote-Teammitglieder freigegeben.
```
$ git add -A
$ git commit -m "Mein Kommentar"
$ git push
```
**How to Push**

Hier habe ich noch einige Befehle die man beherschen sollte. 
```Shell 
$  cd Pfad/zu/meinem/Repository    # Zum lokalen GitHub-Repository wechseln

$  git status                      # Geänderte Datei(en) werden rot aufgelistet
$  git add -A                      # Fügt alle Dateien zum "Upload" hinzu
$  git status                      # Der Status ist nun grün > Dateien sind Upload-bereit (Optional) 
$  git commit -m "Mein Kommentar"  # Upload wird "commited" > Kommentar zu Dokumentationszwecken ist dafür notwendig
$  git status                      # Dateien werden nun als "zum Pushen bereit" angezeigt
$  git push                        #Upload bzw. Push wird durchgeführt
```

---

03 - VirtualBox
======

> [⇧ **Nach oben**](#inhaltsverzeichnis)

Ich habe zuerst Virtualbox installiert
![Virtualbox installed](./Bilder/VirtualBox.png)

Und dannach eine VM manuell erstell
![VM manuell installed](./Bilder/VM-manuell.png)

Hier hatte ich einige Probleme, da in der Anleitung stand das die VM 10 GB an Speicherplatz benötigt, doch ist die mindestanforderung 25GB.
Durch diesen Fehler konnte die VM nicht richtig starten und hatte dauernd einen Fehler.

---

04 - Vagrant
======

> [⇧ **Nach oben**](#inhaltsverzeichnis)

Im Prinzip handelt es sich bei Vagrant um ein Werkzeug, das Software zur Virtualisierung wie VirtualBox oder VMware fernsteuern kann. Auf dem Weg ermöglicht es das automatisierte Erstellen von virtuellen Maschinen an Hand einer zuvor erzeugten Konfigurationsdatei.
![VM automatically installed](./Bilder/Vagrant.png)
Mit dem Befehl vagrant ssh kann man sich dann auf die erstellte VM verbinden und dadurch direkt in der VM Befehle ausführen.
### Vagrant Boxen
Boxen sind vorkonfigurierte (Vorlagen) virtuelle Maschinen für Vagrant. Es wurde entwickelt, um die Softwareverteilung und den Entwicklungsprozess zu beschleunigen. Jede vom Benutzer verwendete Box wird auf dem Computer gespeichert und muss nicht erneut aus dem Internet heruntergeladen werden.

![VagrantBox](./Bilder/vagrantbox.png)

---

05 - Packer
======

> [⇧ **Nach oben**](#inhaltsverzeichnis)

Packer funktioniert ähnlich wie vagrant, kümmert sich aber um die Erstellung von Konfigurationsdateien, die Box-Images enthalten.

![Packer-version](./Bilder/Packer-Version.png)


10 - Fazit
======

> [⇧ **Nach oben**](#inhaltsverzeichnis)

**Tag 1:**
Der erste Tag war sehr theoretisch, aber wir konnten zumindest einen Einblick in die Module bekommen. Die Einführungen waren klar und ich hatte bereits ein Verständnis für jedes Thema. Ich mag den ersten Job, weil man das System ausprobieren und sich einen Überblick verschaffen kann. Aber es gab einige Probleme, bei denen ich bei der manuellen Installation der virtuellen Maschine mit einigen Fehlern konfrontiert war. Ich fand sie und löste sie nach ein wenig Recherche im Internet. Das andere Problem ist, dass, als ich Vagrant zum Installieren der VM verwendete, die Antivirensoftware meinen Plan blockierte und ich die Domäne in vertrauenswürdige Domänen eingeben musste, damit sie erkannt wurde. Der Rest funktioniert einwandfrei und ich konnte etwas Neues lernen.


**Tag2:**
Durch die Repetitionen am Anfang der Stunde konnte ich sehr schnell wieder ins Thema hineinkommen und mich gut konzentrieren. Ich konnte mich sehr gut auf die Aufgaben Fokusieren und hatte dadurch auch Spass daran. Nach einiger Zeit hatte ich schon einiges gemacht und bemerkte das ich langsam nachlasse. Als dann auch noch einige Fehler auftauchten dachte ich mir konzentriere ich mich jetzt ein bisschen auf die Dokumentation. Bei der Dokumentation hatte ich Anfangs kleine Probleme da es für mich das erste mal war das ich auf diese Weise dokumentiert hatte. Nach einiger Zeit hatte ich mich doch noch daran gewöhnt und konnte sehr schnell weiterarbeiten. Ich war sehr zufrieden mit meiner heutigen Leistung. Ich konnte auch sehr viel neues lernen was ich auch in dem Beruf anwenden kann.


**Tag3:**
