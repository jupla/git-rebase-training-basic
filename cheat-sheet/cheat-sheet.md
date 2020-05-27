Cheat-Sheet
===========

Voraussetzungen
---------------

### 0900

Gitg installieren

```
$ sudo apt-get install gitg
```

### 0910

Lokaler Clone - URL kommt von oben rechts!

```
$ git clone git@github.com:(deinFork)/git-rebase-training-basic.git
```

Ablauf
------

### Vorbereitungen

#### 1010

Stelle sicher, dass alle Änderungen am zentralen Repo bei Dir lokal verfügbar sind!

```
$ git fetch --all -p
Fordere an von origin
```

#### 1020

Visualisiere die Situation

```
$ gitg master origin/master experiment origin/experiment
```

![images/start.png](../images/start.png)

### Durchführung

#### 1110

Branch "experiment" auschecken

```
$ git checkout experiment
```

#### 1120

Branch "experiment" aktualisieren

```
$ git pull --rebase
```

#### 1130

Rebase durchführen

```
$ git rebase master
```

#### 1140

Sichten

```
$ gitg master experiment
$ git status
```

#### 1150

Ergebnis "veröffentlichen"

```
$ git push
Username for 'https://github.com': jupla
Password for 'https://jupla@github.com':
To https://github.com/jupla/git-rebase-training-basic.git
! [rejected]        experiment -> experiment (non-fast-forward)
error: Fehler beim Versenden einiger Referenzen nach 'https://github.com/jupla/git-rebase-training-basic.git'
Hinweis: Aktualisierungen wurden zurückgewiesen, weil die Spitze Ihres aktuellen
Hinweis: Branches hinter seinem externen Gegenstück zurückgefallen ist. Führen Sie
Hinweis: die externen Änderungen zusammen (z. B. 'git pull ...') bevor Sie "push"
Hinweis: erneut ausführen.
Hinweis: Siehe auch die Sektion 'Note about fast-forwards' in 'git push --help'
Hinweis: für weitere Details.
```

Veröffentlichung klappt nicht ohne weiteres!
Das ist das erwartete Verhalten an dieser Stelle!
`git rebase` heißt im Normalfall: `git push` klappt nicht!

**Augen auf!**

Jetzt mußt Du Dir sicher sein, dass alles passt!
Sonst gibt's ein Debakel!

```
judith@blackvaio:~/git/git-rebase-training-basic$ git status
Auf Branch experiment
Ihr Branch und 'origin/experiment' sind divergiert,
und haben jeweils 14 und 4 unterschiedliche Commits.
  (benutzen Sie "git pull", um Ihren Branch mit dem Remote-Branch zusammenzuführen)
```

Hierbei ist wichtig:
- Auf Branch **experiment**
- Ihr Branch und 'origin/**experiment**' sind divergiert...

**DU WILLST DIE ZWEIGE NICHT ZUSAMMENFÜHREN!** Also: Kein `git pull` durchführen!
Das würde alles kaputt machen!


Visuelle Kontrolle: "experiment" und "origin/experiment" müssen vorhanden sein

```
$ gitg origin/master master origin/experiment experiment
```

Hier kontrollieren:

- origin/experiment: Hat quasi noch den Vor-Training-Zustand
- experiment: Hat quasi den Zielzustand

Wenn Du die Kontrollen durchgeführt hat und Dir sicher bist,
dass die Erkenntnisse pasen, dann Ergebnis veröffentlichen:

```
$ git push -f
```


Nachkontrolle
-------------

#### 1210

Visualisiere die Situation

```
$ gitg master origin/master experiment origin/experiment
```

<html>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
</html>
