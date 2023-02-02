[HOME](../../README.md) | 01: Arbeiten mit der Shell - Teil 1 | 06: Lab - Linux-Bash-Shell
---
# Lab - Linux-Bash-Shell

1. So überprüfen Sie die Standard-Shell für den aktuellen Benutzer. Zeigen Sie die Shell für den aktuellen Benutzer an, aber nicht unbedingt die Shell, die aktuell ausgeführt wird.
    ```
    $echo $SHELL
    ```
2. So ändern Sie die Shell für Bob von **`Bash`** zu **`Bourne Shell`**
    ```
    $ chsh -s /bin/sh bob
    ```
3. Welchen Wert hat die Umgebungsvariable **`TERM`**
    ```
    echo $TERM
    ```
4. Erstellen Sie eine neue Umgebungsvariable namens **`PROJECT=MERCURY`** und machen Sie sie dauerhaft, indem Sie die Variable zur Datei **`~/.profile`** hinzufügen.
    ```
    echo export PROJECT=MERCURY >> ~/.profile
    ```
5. Welches der folgenden Verzeichnisse ist nicht Teil der PATH-Variablen?
    ```
    /opt/caleston-code
    ```
6. Legen Sie einen Alias namens **`up`** für den Befehl **`uptime`** fest und machen Sie ihn dauerhaft, indem Sie ihn zur Datei **`~/.profile`** hinzufügen.
    ```
    echo alias up=uptime >> ~/.profile
    ```
7. Aktualisieren Sie Bobs Eingabeaufforderung so, dass das Datum im folgenden Format angezeigt wird:
Beispiel: **`[Mi 22. April]bob@caleston-lp10:~$`**
Stellen Sie sicher, dass die Änderung dauerhaft vorgenommen wird.
    ```
    PS1='[\d]\u@\h:\w\$'
    oder
    echo 'PS1=[\d]\u@\h:\w$' >> ~/.profile
    ```
---
[BACK](./05-Bash-Shell.md) | [NEXT](../02-Linux-Core-Konzepte/01-Der-Linux-Kernel.md)
