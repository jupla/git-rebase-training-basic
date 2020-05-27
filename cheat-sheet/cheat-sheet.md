Cheat-Sheet
===========

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
$ git push ...
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
