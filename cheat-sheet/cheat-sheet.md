Cheat-Sheet
===========

Ablauf
------

### Vorbereitungen

#### 0010

Stelle sicher, dass alle Änderungen am zentralen Repo bei Dir lokal verfügbar sind!

```
$ git fetch --all -p
Fordere an von origin
```

#### 0020

Visualisiere die Situation

```
$ gitg master origin/master experiment origin/experiment
```

![images/start.png](../images/start.png)

### Durchführung

#### 0110

Branch "experiment" auschecken

```
$ git checkout experiment
```

#### 0120

Branch "experiment" aktualisieren

```
$ git pull --rebase
```

#### 0130

Rebase durchführen

```
$ git rebase master
```

#### 0140

Sichten

```
$ gitg master experiment
$ git status
```

#### 0150

Ergebnis "veröffentlichen"

```
$ git push ...
```

Nachkontrolle
-------------

#### 0210

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
