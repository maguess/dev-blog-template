# Inhalt der Checkliste

## Table of Contents
- [Projektabgabe - <code><font color="red">**V-Server einrichten**</font></code>](#projektabgabe---codefont-colorredv-server-einrichtenfontcode)
  - [Einrichtung des V-Servers](#1-einrichtung-des-v-servers)
    - [Aufgaben](#aufgaben)
  - [Hinweise](#2-hinweise)
    - [Allgemeine Hinweise](#allgemeine-hinweise)
    - [Sicherheitshinweise](#sicherheitshinweise)
    - [Testing](#testing)
  - [Dokumentation](#3-dokumentation)
    - [Git-Repository mit README](#git-repository-mit-readme) 
  

# Projektabgabe - <code><font color="red">**V-Server einrichten**</font></code>

Bitte erfülle alle Punkte auf dieser Liste, bevor du das Projekt einreichst. Solltest du weitere Extras eingebaut haben,
erwähne das kurz, damit sich die Mentoren dies bei Bedarf anschauen können.   
**Beachte** dazu auch die Sektion [Dokumentation](#3-dokumentation) am Ende dieses Dokuments.

Hilfestellung zur Abgabe und Umsetzung dieses Projektes findest du auf der [DevSecOps FAQ Seite.](https://developer-akademie-devsecopskurs.github.io/dso-faq-site/de/docs/category/v-server-setup)


## 1. Einrichtung des V-Servers

### Aufgaben

- [x] Füge deinen SSH Public Key zu den authorized_keys deines 
  Benutzers hinzu. Dafür kann das Programm ssh-copy-id aus
  der Kommandozeile auf dem eigenen Computer verwendet werden.  
  - [x] Das Key-Pair, welches du für die Interaktion mit deinem Server benutzen willst, solltest du auf deinem Computer 
    generieren \- **nicht** auf dem Server.  
- [x] Deaktiviere den Passwort-Login auf dem Server  
  - [x] Stelle sicher, dass ein Login mit einem SSH-Key erfolgreich funktioniert hat, **bevor** du den Passwort-Login 
    deaktivierst  
- [x] Installiere den Webserver NGINX  
- [x] Verändere die Konfiguration von NGINX, sodass eine alternative HTML-Seite als Einstiegspunkt angezeigt wird. 
  Gegebenenfalls muss hierzu NGINX neu gestartet werden  
- [x] Konfiguriere git auf deinem V-Server so, dass dein Nutzername und deine E-Mail-Adresse hinterlegt sind. 
  Die Benutzerdaten sollten den Daten auf deinem Computer entsprechen, bzw. deckungsgleich mit deinen in GitHub 
  hinterlegten Daten sein.  
  - [x] Um die Konfiguration für Git und GitHub vollständig abzuschließen, solltest du ein SSH-Key-Pair auf deinem 
    Server anlegen, sodass du den Public Key in GitHub hinterlegen kannst, um von deinem Server aus Repositories auf den
    Server zu pullen und mit ihnen zu interagieren.

## 2. **Hinweise**

### **Allgemeine Hinweise**

- [x] Zusätzlich zu deinem GitHub Repository solltest du ein kurzes Loom Video (maximal 5min.) aufnehmen und 
  bereitstellen, indem du kurz deine Abgabe zeigst und vorstellst, was du getan hast \- dabei musst du nicht alle 
  Details erwähnen, jedoch sollst du auf alle relevanten Schritte kurz eingehen und diese zeigen

### **Sicherheitshinweise**

- [x] Stelle sicher, dass ein Login mit einem SSH-Key erfolgreich funktioniert hat, **bevor** du den Passwort-Login 
  deaktivierst

### **Testing**

Bevor du dein Projekt einreichst, solltest du die folgenden Dinge sichergestellt und getestet haben:

- [x] Ich habe die [FAQ Seite](https://developer-akademie-devsecopskurs.github.io/dso-faq-site/de/docs/projects/vserver-setup/faq) für dieses Projekt durchgelesen und alle Punkte umgesetzt  
- [x] Es wird das bereits vorhandene Docusaurus Projekt genutzt  
- [x] Es gibt einen Feature Branch und einen Pull Request in DEINEM Docusaurus Repo  
- [x] Dieser Pull Request enthält eine Ordnerstruktur, die folgendermaßen aussehen sollte: 
  /docs/v-server/ mit einer
  README.md   
- [x] In dieser README.md ist deine technische Dokumentation beschrieben  
- [x] Man kann sich mit Hilfe eines SSH-Keys auf dem Server anmelden  
- [x] Man kann sich **nicht** mit einer Kombination aus Nutzernamen und Passwort anmelden  
  - [x] Hierzu kann die SSH-Option \-o PubKeyAuthentication=no 
   hilfreich sein z.B. ssh \-o PubKeyAuthentication=no \-i pfad/zum/
   private-key user@12.34.67.89  
- [x] Teste die Verfügbarkeit deines Webservers, indem du die IP-Adresse des V-Servers in deinen Browser in der 
  Adresszeile eingibst und die Eingabe bestätigst. Du solltest dann einen Willkommens-Bildschirm von NGINX angezeigt 
  bekommen  
  - [x] Bevor du die Konfiguration anwendest, kannst du diese mithilfe von   
    nginx \-t  validieren (deine Konfiguration liegt unter
    /etc/nginx/nginx.conf)  
  - [x] Falls du eine eigene Konfigurationsdatei für nginx hast, dann kannst du diese folgendermaßen isoliert testen:  
    nginx \-t \-c pfad/zur/config  
- [x] Validiere, dass die neue Konfiguration von deinem NGINX Server angewendet wird und im Browser dementsprechend 
  deine HTML-Seite zu sehen ist

## 3. **Dokumentation**

### **Git-Repository mit README**

- [x] Die Dokumentation soll auf Englisch geschrieben werden.  
- [x] Achte darauf, dass du nicht sicherheitskritische Inhalte wie dein Passwort oder den Inhalt deiner SSH Keys in 
  das Repository schreibst.  
- [x] Die README Datei sollte in Markdown Format geschrieben und ordentlich strukturiert sein  
- [x] Eine Inhaltsangabe sollte vorhanden sein  
- [x] Die einzelnen Schritte sollten jeweils in einer Sektion, oder ggf. auch in einem eigenen Dokument beschrieben 
  sein. Bei mehreren Dokumenten sollten diese sinnvoll miteinander verlinkt sein.  
- [x] Diese Checkliste sollte ebenfalls als PDF im Repository enthalten sein.

Bei deiner Abgabe solltest du am besten auch die IP-Adresse deines V-Servers mit angeben, sodass die Mentoren dort auch 
die Konfiguration überprüfen können.