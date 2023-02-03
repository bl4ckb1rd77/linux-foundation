[HOME](../../README.md) | 02: Linux Core Konzepte | 03: Lab Linux Kernel
---
# Lab - Linux-Kernel

Um die genaue Kernel-Version zu überprüfen, die in diesem System ausgeführt wird.
```
$ uname -r
```

was ist die Kernel-Version in 5.15.0-58-generic?
```
Suchen Sie nach der ersten Ziffer. In diesem Fall sind es 5
```

Wie lautet die Hauptversionsnummer des Kernels 5.15.0-58-generic
```
Suchen Sie nach der zweiten Ziffer nach der Kernel-Version, getrennt durch ein . In diesem Fall sind es 15
```

Welchen Befehl würden Sie ausführen, um die vom Kernel generierten Meldungen auszudrucken?
```
Geben Sie den Befehl dmesg ein, um die Meldungen anzuzeigen.
$ dmesg
```

Zum Auflisten/Zählen aller im System vorhandenen Blockgeräte vom Typ Disk
```
Führen Sie aus: lsblk und zählen Sie die Anzahl der Festplattengeräte.
$ lsblk
```

Um die Gesamtzahl der **`physischen Kerne`** im System zu überprüfen.
```
Führen Sie lscpu aus und multiplizieren Sie die Cores pro Socket mit der Anzahl der Sockets:
$ lscpu
```

Zum Überprüfen des gesamten Online-Speichers
```
Führen Sie den Befehl lsmem aus und suchen Sie nach dem Wert des Online-Speichers
$lsmem
```
---
[BACK](./02-Arbeiten-mit-der-Hardware.md) | [NEXT](./04-Linux-Boot-Sequenz.md)
