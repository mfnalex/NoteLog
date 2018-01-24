# NoteLog
Indexbasiertes Notizbuch für die BASH

## Benutzung
Der Aufruf von notelog ohne Parameter werden alle angelegten Notizen gezeigt. Eine spezielle Notiz kann mit ```notelog get <name>``` angezeigt werden. Neue Notizen können mit ```notelog set <name> <inhalt>``` angelegt werden. Bestehende Notizen werden nur überschrieben, wenn ```setf``` anstatt ```set``` benutzt wird (```notelog setf <name> <neuerInhalt>```). Eine Notiz kann gelöscht werden mit ```notelog rm <name>``` bzw. ```notelog del[ete] <name>```.
