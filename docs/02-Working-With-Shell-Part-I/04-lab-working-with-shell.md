# Lab - Arbeiten mit der Shell

1. Um das Home-Verzeichnis für einen bestimmten Benutzer zu überprüfen, sagen Wir für **`bob`**
    ```
    $ grep bob /etc/passwd | cut -d ":" -f6
    ```
1. Um das Home-Verzeichnis für einen bestimmten Benutzer zu überprüfen, verwenden Sie eingebaute Shell-Variablen
    ```
    $echo $HOME
    ```
1. Was bedeutet das Wort Willkommen im Befehl **`echo Willkommen`** in Bezug auf den Befehl?
    ```
    $ echo Willkommen
      - Wo Willkommen ein Argument ist
    ```

1. Um den Befehlstyp **`git`** zu überprüfen
    ```
    $ type git
    ```
1. So erstellen Sie ein Verzeichnis
    ```
    $ mkdir /home/bob/birds
    ```
1. Um Verzeichnisse rekursiv zu erstellen
    ```
    $ mkdir -p /home/bob/fish/lachs
    ```
1. Erstellen Sie einige weitere Verzeichnisse
    ```
    $ mkdir -p /home/bob/mammals/elephant
    $ mkdir -p /home/bob/mammals/monkey
    $ mkdir /home/bob/birds/eagle
    $ mkdir -p /home/bob/reptile/snake
    $ mkdir -p /home/bob/reptile/frog
    $ mkdir -p /home/bob/amphibian/salamander
    ```
1. Zum Verschieben eines Verzeichnisses
    ```
    $ mv /home/bob/reptile/frog /home/bob/amphibien
    ```
1. Um ein Verzeichnis umzubenennen
    ```
    $ mv /home/bob/reptile/snake /home/bob/reptile/crocodile
    ```
1. Zum Löschen eines Verzeichnisses
    ```
    $ rm -r /home/bob/reptil
    ```
