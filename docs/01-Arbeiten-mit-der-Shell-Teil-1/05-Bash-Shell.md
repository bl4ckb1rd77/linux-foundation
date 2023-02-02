# Bash-Shell

## Verschiedene Arten von Shell

In diesem Abschnitt werden wir uns verschiedene Arten von Shells ansehen.
- Es gibt verschiedene Arten von Shells in Linux, einige der beliebtesten sind unten aufgeführt
   - Bourne-Shell (sh)
   - C-Shell (csh oder tsh)
   - Korn Shell (ksh)
   - Z-Shell (zsh)
   - Bourne Again-Shell (Bash)

Um die verwendete Shell zu überprüfen. Verwenden Sie den Befehl **`echo $SHELL`**
```bash
$echo $SHELL
```

So ändern Sie die Standard-Shell. Verwenden Sie den Befehl chsh, Sie werden nach dem Passwort gefragt und geben anschließend den Namen der neuen Shell ein. Sie müssen sich jedoch bei einer neuen Terminalsitzung anmelden, um diese Änderung zu sehen.
```
$chsh
```

## Bash-Shell-Funktionen

1. Bash unterstützt die automatische Vervollständigung von Befehlen. Dies bedeutet, dass bash Befehle für Sie automatisch vervollständigt, wenn Sie einen Teil davon eingeben und die **`Tab`**-Taste drücken
    ```bash
    [~]$ ls /etc/pas
    ````
    Tab Taste drücken
    ```bash
    [~]$ ls /etc/passwd
    ```
1. In Bash können wir benutzerdefinierte Aliase für die eigentlichen Befehle festlegen
    ```bash
    $ date
    $ alias dt=date
    $ dt
    ```
1. Verwenden Sie den Befehl **`history`**, um die vorherigen Ausführungsbefehle aufzulisten, die Sie zuvor ausgeführt haben
    ```bash
    $ history
    ```

  ## Bash-Umgebungsvariablen

  Umgebungsvariable **`SHELL`** drucken
  ```bash
  $echo $SHELL
  ```

  Um eine Liste aller Umgebungsvariablen anzuzeigen. Führen Sie **`env`** vom Terminal aus
  ```bash
  $ env
  ```

  Um eine Umgebungsvariable mit in der Shell zu setzen. Der Wert wird nicht auf andere Prozesse übertragen.
  ```bash
  $ OFFICE=Koeln
  ```

  Um eine Umgebungsvariable festzulegen, können wir den Befehl **`export`** verwenden. Um den Wert auf einen anderen Prozess zu übertragen.
  ```bash
  $ export OFFICE=Koeln
  ```

  Um eine Umgebungsvariable über eine nachfolgende Anmeldung oder einen Neustart dauerhaft zu setzen, fügen Sie sie zu **`~/.profile`** oder **`~/.pam_environment`** im Home-Verzeichnis des Benutzers hinzu.

  ```bash
  $ echo "export OFFICE=Koeln" >> ~/.profile (oder)
  $ echo "export OFFICE=Koeln" >> ~/.pam_environment
  ```

  So überprüfen Sie den Wert einer Umgebungsvariablen namens **`LOGNAME`**
  ```bash
  $echo $LOGNAME
  ```

## Pfadvariable

#### Apropos Umgebungsvariablen: Wenn ein Benutzer einen externen Befehl in die Shell eingibt, verwendet die Shell die Pfadvariable, um nach diesen externen Befehlen zu suchen

Um die in der Pfadvariablen definierten Verzeichnisse anzuzeigen. Verwenden Sie den Befehl **`echo $PATH`**.
```bash
$echo $PATH
```

Um zu prüfen, ob der Ort des Befehls identifiziert werden kann. Verwenden Sie den **`which`**-Befehl

**`Syntax: which <Befehl>`**

```bash
$ which pulsar
```

Um einen Befehl in der **`PATH`**-Variablen zu definieren. Zum Hinzufügen können wir den Befehl **`export`** verwenden.
```bash
$ export PATH=$PATH:/opt/pulsar/bin
$ which pulsar
```

## Bash-Eingabeaufforderung anpassen

Sobald Sie sich in die Shell einloggen, ist die Zeile, die Sie sehen, die Bash-Eingabeaufforderung.

```bash
[~]$
```
`~ = Aktuelles Arbeitsverzeichniss`\\\
`$ = User Prompt Symbol`

Es kann angepasst werden, um den **`username`** und den **`hostname`** anzuzeigen
```bash
[michael@prod-server]$
```

#### Der Bash-Prompt wird durch eine Reihe spezieller Shell-Umgebungsvariablen gesteuert. Die häufigste davon und diejenige, auf die wir uns konzentrieren werden, ist die Variable **`PS1`**.

```bash
[~]$ echo $PS1
[\W]$
```
`\W = Aktuelles Arbeitsverzeichniss = ~`\\\
`$ = User Prompt Symbol`

Geben Sie **`echo $PS1`** ein, um den **`PS1`** zugewiesenen Wert anzuzeigen
```bash
$echo $PS1
```

Um die PS1 so zu ändern, dass nur das Wort **`ubuntu-server`** angezeigt wird.
```bash
$ PS1="ubuntu-server"
$echo $PS1
```

#### Zur weiteren Anpassung sehen Sie sich das folgende Sonderzeichen an.

```bash
[~]$ PS1="ubuntu-server:"
ubuntu-server:
```
```bash
ubuntu-server: echo $PS1
ubuntu-server:
```
```bash
ubuntu-server: PS1="[\d \t \u@\h:\w] $ "
[Mon Jan 23 11:14:13 michael@prod-server:~] $
```

Spezielle Prompt Variablen:
```bash
\d   The date, in "Weekday Month Date" format (e.g., "Tue May 26").

\h   The hostname, up to the first . (e.g. deckard)
\H   The hostname. (e.g. deckard.SS64.com)

\j   The number of jobs currently managed by the shell.

\l   The basename of the shell's terminal device name.

\s   The name of the shell, the basename of $0 (the portion following the final slash).

\t   The time, in 24-hour HH:MM:SS format.
\T   The time, in 12-hour HH:MM:SS format.
\@   The time, in 12-hour am/pm format.

\u   The username of the current user.

\v   The version of Bash (e.g., 2.00)

\V   The release of Bash, version + patchlevel (e.g., 2.00.0)

\w   The current working directory.
\W   The basename of $PWD.

\!   The history number of this command.
\#   The command number of this command.

\$   If you are not root, inserts a "$"; if you are root, you get a "#"  (root uid = 0)
```

Um die Bash-Eingabeaufforderung so zu ändern, dass sie **`date`**, **`time`**, **`Benutzername des aktuellen Benutzers`**, den **`Hostnamen`** und die **`aktuelle Arbeits Verzeichnis`**
```
$ PS1 = "[\d \t \u@\h:\w ] $ "
```
