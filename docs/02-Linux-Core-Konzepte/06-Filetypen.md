# Dateitypen unter Linux

In diesem Abschnitt werfen wir einen Blick auf verschiedene Dateitypen unter Linux.
- Alles ist eine Datei in Linux.
   - Jedes Objekt in Linux kann als Dateityp betrachtet werden, sogar ein Verzeichnis ist beispielsweise ein spezieller Dateityp.

Es gibt drei Arten von Dateien.
1. Normale Datei
1. Verzeichnis
1. Spezielle Dateien

![Dateitypen](../../images/Dateitypen.PNG)

**`Spezielle Dateien`** werden wiederum in fünf andere Dateitypen kategorisiert.
1. Character Files
    - Diese Dateien stellen Geräte unter dem Dateisystem **`/dev`** dar.
    - Beispiele hierfür sind Geräte wie die **`Tastatur`** und die **`Maus`**.
1. Block Files
    - Diese Dateien stellen Blockgeräte dar, die sich auch im Dateisystem **`/dev/`** befinden.
    - Beispiele sind die **`Festplatten`** und **`RAM`**
1. Links
    - Links in Linux sind eine Möglichkeit, zwei oder mehr Dateinamen mit demselben Satz von Dateidaten zu verknüpfen.
    - Es gibt zwei Arten von Links
      - Die harte Verbindung
      - Der weiche Link
1. Sockets
    - Ein Sockets ist eine spezielle Datei, die die Kommunikation zwischen zwei Prozessen ermöglicht.
1. Named Pipes
    - Named Pipes ist ein spezieller Dateityp, der es ermöglicht, einen Prozess als Eingabe für einen anderen zu verbinden

      ![Dateitypen1](../../images/Dateitypen1.PNG)

#### Sehen wir uns nun an, wie man unter Linux verschiedene Dateitypen erkennt.

Eine Möglichkeit, einen Dateityp zu identifizieren, ist die Verwendung des **`file`**-Befehls.
```
$ file /home/michael
$ file bash-script.sh
$ file /var/run/snapd.socket
$ file /home/michael/bash-script.sh
```

Eine andere Möglichkeit, einen Dateityp zu identifizieren, ist die Verwendung des Befehls **`ls -ld`**
```
ls -ld /home/michael
ls -l bash-script.sh
```
    ![Dateitypen2](../../images/Dateitypen2.PNG)
