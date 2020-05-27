Training: Git-Rebase (grundlegend)
==================================

Dies ist das grundlegende Training zu Git-Rebase.
Es dient dazu, dass Du Erfahrungen im Umgang mit
Git-Rebase sammelst.

Das Training ist intern und extern verfügbar.
Die externe URL ist: [github:git-rebase-training-basic](https://github.com/70435-training/git-rebase-training-basic).

Voraussetzungen
---------------

Seitens der "Infrastruktur" gibt es diese Voraussetzungen:

* Firefox ist installiert (Chrome geht nicht)
* Git-Kommandozeilen-Tools sind installiert
* Gitg ist installiert [Wie?](cheat-sheet/cheat-sheet.md#0900)
* Fork von diesem Repo ist angelegt, Arbeit erfolgt nur an
  diesem Fork
* Du hast einen lokalen Clone vom Fork [Wie?](cheat-sheet/cheat-sheet.md#0900)
* Dein Arbeitsverzeichnis ist im lokalen Clone
* Diese Anleitung kann in Firefox gesichtet werden: `firefox index.html`

Seitens der Kenntnisse:

* Erfahrung mit der Kommandozeile
* Erfahrung mit Git (clone, branch, pull/push, commit, ...)

Ausgangsituation
----------------

![Ausgangssituation](images/start.png)

- Es gibt einen Master-Branch
- ... und auch den Branch "experiment"
- "experiment" wurde irgendwann in der Vergangenheit erzeugt,
  er zweigt in der Vergangenheit vom Master-Branch ab
- Die Ausgangssituation kannst Du visualisieren mit `gitg origin/master origin/experiment`

Zielbild
--------

![Zielsituation](images/final.png)

- Es gibt einen Master-Branch
- ... und auch den Branch "experiment"
- Der Abzweigezeitpunkt von "expriment" ist verschoben
  auf den aktuellen Master-Branch

Ablauf
------

### Vorbereitungen

- Öffne dieses Dokument in Firefox mit `firefox index.html`,
  damit Du direkten Zugriff auf die "cheat sheets" bekommen kannst
  (Chrome geht nicht, Browsen via Github o.ä. geht nicht)
- Stelle sicher, dass alle Änderungen am zentralen Repo bei Dir lokal verfügbar sind [Wie?](cheat-sheet/cheat-sheet.md#1010)
- Visualisiere die Situation [Wie?](cheat-sheet/cheat-sheet.md#1020)
- Kontrolliere, ob "master" und "origin/master" übereinstimmen!
- Kontrolliere, ob "experiment" und "origin/experiment" übereinstimmen!

### Durchführung

- Branch "experiment" auschecken [Wie?](cheat-sheet/cheat-sheet.md#1110)
- Branch "experiment" aktualisieren [Wie?](cheat-sheet/cheat-sheet.md#1120)
- Rebase durchführen [Wie?](cheat-sheet/cheat-sheet.md#1130)
- Sichten [Wie?](cheat-sheet/cheat-sheet.md#1140)
- Ergebnis "veröffentlichen" [Wie?](cheat-sheet/cheat-sheet.md#1150)

Nachkontrolle
-------------

- Visualisiere die Situation [Wie?](cheat-sheet/cheat-sheet.md#1210)
- Kontrolliere, ob "master" und "origin/master" übereinstimmen!
- Kontrolliere, ob "experiment" und "origin/experiment" übereinstimmen!
- Vergleiche Dein Bild strukturell mit [images/final.png](images/final.png)

Abschluß
--------

Nach Abschluß des Trainings bitte die URL zu dem bearbeiteten
Fork per Email schicken an "dp-training@daemons-point.com"!
