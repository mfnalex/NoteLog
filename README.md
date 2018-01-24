# NoteLog
Indexbasiertes Notizbuch für die BASH

## Installation
```
wget https://raw.githubusercontent.com/mfnalex/NoteLog/master/notelog
chmod +x notelog
sudo mv notelog /usr/local/bin/
```

## Benutzung
Mit ```notelog help``` werden alle verfügbaren Optionen aufgelistet.

Der Aufruf von notelog ohne Parameter werden alle angelegten Notizen gezeigt. Eine spezielle Notiz kann mit ```notelog get <name>``` angezeigt werden.

Neue Notizen können mit ```notelog set <name> <inhalt>``` angelegt werden. Bei der Eingabe können Platzhalter benutzt werden (siehe unten).

Notizen können auch Sonderzeichen wie z.B. einen Zeilenumbruch enthalten. Dann muss der Inhalt in doppelten Anführungszeichen übergeben werden und escaped werden. Beispiel: ```notelog setf multiline "Diese Notiz enthält direkt mehrere Zeilen.\n\nDas hier ist die Vierte."```

Bestehende Notizen werden nur überschrieben, wenn ```setf``` anstatt ```set``` benutzt wird (```notelog setf <name> <neuerInhalt>```).

Eine Notiz kann gelöscht werden mit ```notelog rm <name>``` bzw. ```notelog del[ete] <name>```.

## Verfügbare Platzhalter
Im Inhalt der Notizen können folgende Platzhalter benutzt werden, die automatisch durch ihr jeweiliges Äquivalent ersetzt werden:

| Name          | Alias         | wird umgewandelt zu                                      |
| ------------- |---------------| ---------------------------------------------------------|
| `:date:`      | `:datum:`     | Aktuelles Datum (TT.MM.JJJJ)                             |
| `:time:`      | `:zeit:`      | Aktuelle Uhrzeit (HH:MM:SS)                              |
| `:now:`       | `:jetzt:`     | Aktuelles Datum + Uhrzeit inkl. Zeitzone und Wochentag   |
