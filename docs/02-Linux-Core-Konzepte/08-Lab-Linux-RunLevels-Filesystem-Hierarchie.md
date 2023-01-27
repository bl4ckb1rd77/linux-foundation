# Lab - Linux Runlevels und Dateisystemhierarchie

Zum Ausführen von Befehlen, die **`sudo`**(Superuser)-Berechtigungen benötigen. Führen Sie **`sudo`** aus
```
$ sudo ls /root
```

Um den vom System verwendeten **`Init-Prozess`** (systemd oder sysV) zu überprüfen
```
$ sudo ls -l /sbin/init
```

Um das im System festgelegte **`standardmäßige systemd-Ziel`** (z. B. graphic.target oder multi-user.target) zu überprüfen
```
$ sudo systemctl get-default
```

So ändern Sie das systemd-Ziel in **`multi-user.target`**
```
$ sudo systemctl set-default multi-user.target
```

Um zu überprüfen, welcher Dateityp **`firefox.deb`** ist, der sich unter /root befindet
```
$ sudo file /root/firefox.deb
```

Um zu überprüfen, welcher Dateityp **`sample_script.sh`** ist, das sich unter /root befindet
```
$ sudo file /root/sample_script.sh
```

Sie wurden aufgefordert, eine neue **`Drittanbieter-IDE`** im System zu installieren. Welches Verzeichnis ist die empfohlene Wahl für die Installation?
```
Software von Drittanbietern wird normalerweise unter **`/opt`** installiert
```

Welches Verzeichnis enthält die Dateien, die sich auf die Blockgeräte beziehen, die beim Ausführen des Befehls **`lsblk`** angezeigt werden?
```
Block Device- oder Device Node-Dateien befinden sich im Verzeichnis **`/dev`**
```

Wie lautet der Name des **`Anbieters`** für den **`Ethernet-Controller`**, der in diesem System verwendet wird?
```
Verwenden Sie: sudo lshw und suchen Sie den Anbieter für den Ethernet-Controller im Netzwerkabschnitt.
$ sudo lshw
```
