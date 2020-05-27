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

Server ist aufgesetzt (inkl. Apache) und hier kommt der völlig überflüssige Text.
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


#### Anpassungen im Puppet4 Repository puppet_site - Änderung erfolgt auch hier  

Zum Einlesen der Properties werden die entsprechenden Klassen im feature branch *puppet_site*
implementiert.    

1. Wechsel zum Verzeichnis puppet_site    
2. Puppet4 Repository puppet_site -> Branch anlegen    
   Individuellen Branch anlegen. Hierzu zuerst auf Branch *production* wechseln.   
   **ACHTUNG:** Branch für puppet_site muss immer von "origin/production" abzweigen.    
   Sollte dies nicht der Fall sein, wird der Pull Request von den MOMs abgelehnt.    
3. Prüfung, welche Dateien existieren bereits im Projekt (Module): **tur**   
   Speziell "Profile" und "Role" sind für den Tomcat Aufbau notwendig    
4. Anpassen des Profile für Tomcat turmasterdata -> puppet_site/site/profile/manifests/tur/    
   Als Basis die Datei "turqpp.pp" heranziehen und im Text "turqpp" durch "turmasterdata" ersetzen -> Datei "turmasterdata.pp"   
   `judith@blackvaio:~/projects/puppet/puppet_site/site/profile/manifests/tur$ sed -e "s/turqpp/turmasterdata/g" ./turqpp.pp > ./turmastertest.pp`     
5. Anpassen der "Role" für den Tomcat turmasterdata -> Datei: *puppet_site/site/role/manifests/tur/app.pp* bearbeiten  
   Hinzufügen der Zeile "profile::tur::turmasterdata," für den Tomcat turmasterdata     
6. Änderungen in Git einchecken   
7. Wechsel auf Freeway Server  -> https://freeway.porsche.org/webapp/puppet_site -> Anmelden   
8. Linke Seite -> Merge Requests -> individuellen Branch aus Liste auswählen    
9. Button "Create Merge Request" > Merge nach **development**  -> Merge Request erstellen  
10. Mail an "fwmerge@daemons-point.com" > Betreff: Pull Request für <XXXXXX> > Angabe der URL des Merge Requests zum Reviewen
11. Review wurde durchgeführt (Daumen hoch) > Merge durchführen (Button: Merge)    
    **ACHTUNG:** unbedingt **development** als Ziel für den Merge auswählen, da die Änderung zuerst auf der E-Umgebung benötigt wird.   
    Bei Neuaufbauten muss danach jeweils ein weiterer Merge Request für **testing**, **preprod** (manchmal) und für **production** erstellt werden.
