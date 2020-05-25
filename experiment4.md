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


<!-- TEASER_END -->

Voraussetzung Änderung erfolgt im Master
--------------

Server ist aufgesetzt (inkl. Apache) und 
es existiert bereits mindestens 1 Tomcat auf dem Server.


Tomcat Aufbau
-------------

## Beispiel: TuR Tomcat Aufbau - wird sehr schön

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

1. Wechsel zum Verzeichnis puppet_site  - sieht gut aus  
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
