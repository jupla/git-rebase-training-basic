<!--
.. title: TuR: Tomcat Aufbau
.. date: 2018-11-19 09:00:00
.. tags: tur, puppet4
.. category: TuR
.. link:
.. description:
.. type: text
.. author: Judith Platzer
-->

<!--
TuR: Tomcat Aufbau
==================
-->

<div id="toc" />

Hier beschreibe ich, wie ein Tomcat Aufbau E-Umgebung zu erfolgen hat.     
Detailbeschreibung mit viel mehr Details findest du [hier (puppet4-tomcat-aufbau-detailbeschreibung.md)](puppet4-tomcat-aufbau-detailbeschreibung.md)  
Weiterführende Informationen zum Tomcat Aufbau findest du [hier (puppet4-tomcat-aufbau-erweiterung.md)](puppet4-tomcat-aufbau-erweiterung.md)

<!-- TEASER_END -->

Voraussetzung
--------------

Server ist aufgesetzt (inkl. Apache) und 
es existiert bereits mindestens 1 Tomcat auf dem Server.


Tomcat Aufbau
-------------

## Beispiel: TuR Tomcat Aufbau

**Aufgabe:** Tomcat turmasterdata analog turqpp auf dezuepagap099 aufbauen

**Informationen:**  
* TuR E-Umgebung Server: dezuepagap099.porsche.org
* Tomcat turmasterdata aufbauen
* Tomcat turqpp existiert bereits   

## Ablauf

### Voraussetzungen

* puppet_site ist ausgecheckt im Verzeichnis "projects/puppet/puppet_site"
* puppet_hiera ist ausgecheckt im Verzeichnis "projects/puppet/puppet_hiera"


### Kurzbeschreibung der Aktionen


#### Anpassungen im Puppet4 Repository puppet_site   

Zum Einlesen der Properties werden die entsprechenden Klassen im feature branch *puppet_site*
implementiert.    

f abwarten)
3. Dummy-War-File *dp-basic-v1.3.war* von dpserv.emea.porsche.biz:/home/uli auf dezuepagap099 kopieren.
4. war-File in Verzeichnis */srv/stage* kopieren 
5. Tomcat turmasterdata neu starten  
6. Der Tomcat turmasterdata wurde durchgestartet und läuft!        

Prüfung der WebMon CheckURL zum Schluß
