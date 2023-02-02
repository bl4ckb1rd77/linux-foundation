[HOME](../../README.md) | 01: Arbeiten mit der Shell - Teil 1 | 03: Verwenden der Befehlszeile, um Hilfe zu erhalten
---
# Verwenden der Befehlszeile, um Hilfe zu erhalten

In diesem Abschnitt lernen wir, wie man den Befehl **`help`** verwendet, um Hilfe in der Befehlszeile zu erhalten
- Wenn Sie neu in der Verwendung von "Linux" oder "Bash Shell" sind oder wenn Sie nicht sicher sind, welcher Befehl was tut, gibt es einige Befehle in Bash, die Ihnen beim Einstieg helfen können.
- Werfen wir einen Blick darauf

Der erste Befehl ist **`whatis`** , dieser Befehl zeigt eine einzeilige Beschreibung eines Befehls an.

**`Syntax: whatis <Befehl>`**

```
$ whatis date
```

Die meisten der internen oder externen Befehle werden mit **`Manpages`** geliefert, die detaillierte Informationen über den Befehl enthalten (mit Beispielen, Anwendungsfällen und mit Befehlsoptionen).

**`Syntax: man <Befehl>`**

```
$ man date
```

Mehrere Befehle stellen **`-h`** oder **`--help`** bereit, um Benutzern die in einem Befehl verfügbaren Optionen und Anwendungsfälle bereitzustellen

```
$ uptime -h
$ uptime --help
```

Verwenden Sie **`apropos`**, um die Manpage-Namen und -Beschreibungen nach Instanzen des Schlüsselworts zu durchsuchen. Dies ist nützlich, wenn Sie nach allen Befehlen innerhalb des Systems suchen möchten, die das bestimmte Schlüsselwort enthalten.

**`Syntax: apropos <Schlüsselwort>`**
```
$ apropos modpr
```
---
[BACK](./02-Basis-Befehle.md) | [NEXT](./04-lab-working-with-shell.md)
