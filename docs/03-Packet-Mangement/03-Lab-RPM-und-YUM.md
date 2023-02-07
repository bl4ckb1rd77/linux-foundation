[HOME](../../README.md) | 03: Packet Management | 03: Lab RPM und YUM
---
# Lab - RPM and YUM

Welche Paketmanager würden Sie auf der Rocky-Maschine verwenden?
```
Rocky verwendet RPM and YUM
```

Verwenden Sie einen **`rpm`**-Befehl und finden Sie den genauen Paketnamen für **`wget`** heraus, das auf diesem Server installiert ist
```
$ rpm -qa |grep wget
```

So installieren Sie ein Paket für den **`firefox`**-Browser, das unter **`/home/bob`** im System heruntergeladen wurde. Achtung: Es kann aufgrund fehlgeschlagener Abhängigkeiten fehlschlagen
```
$ sudo rpm -ivh /home/bob/firefox-68.6.0-1.el7.centos.x86_64.rpm
```

So installieren Sie ein Paket für den **`firefox`**-Browser zusammen mit seinen Abhängigkeiten
```
$ sudo yum install firefox -y
```

Um zu überprüfen, wie viele Software-Repositories für YUM im System konfiguriert sind
```
$ sudo yum repolist
```

Um zu überprüfen, welches Paket den Befehl **`tcpdump`** bereitstellt
```
$ sudo yum provides tcpdump
```
---
[BACK](./02-RPM-und-YUM.md) | [NEXT](./04-DPKG-und-APT.md)
