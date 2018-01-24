# NoteLog
Indexbasiertes Notizbuch für die BASH

## Installation
```
wget https://raw.githubusercontent.com/mfnalex/NoteLog/master/notelog
chmod +x notelog
sudo mv notelog /usr/local/bin/
```

## Benutzung
Der Aufruf von notelog ohne Parameter werden alle angelegten Notizen gezeigt. Eine spezielle Notiz kann mit ```notelog get <name>``` angezeigt werden.
Neue Notizen können mit ```notelog set <name> <inhalt>``` angelegt werden.
Bestehende Notizen werden nur überschrieben, wenn ```setf``` anstatt ```set``` benutzt wird (```notelog setf <name> <neuerInhalt>```).
Notizen können Sonderzeichen wie z.B. einen Zeilenumbruch enthalten. Dann muss der Inhalt in doppelten Anführungszeichen übergeben werden und escaped werden (Beispiel: ```notelog setf multiline "Diese Notiz enthält direkt mehrere Zeilen.\n\nDas hier ist die Vierte."```)
Eine Notiz kann gelöscht werden mit ```notelog rm <name>``` bzw. ```notelog del[ete] <name>```.
