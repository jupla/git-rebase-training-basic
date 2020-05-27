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

![images/start.png](images/start.png)

### Durchführung

#### 0110

```
$ git checkout experiment
```

#### 0120

```
$ git pull --rebase
```

#### 0130

```
$ git rebase master
```

#### 0140

```
$ gitg master experiment
$ git status
```

#### 0150

```
$ git push ...
```

Nachkontrolle
-------------

#### 0210

```
$ gitg master origin/master experiment origin/experiment
```
