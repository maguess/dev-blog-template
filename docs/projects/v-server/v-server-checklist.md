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

- [ ] Füge deinen SSH Public Key zu den <span style="background-color: lightgrey;">authorized_keys</span> deines 
  Benutzers hinzu. Dafür kann das Programm <span style="background-color: lightgrey;">ssh-copy-id</span > aus
  der Kommandozeile auf dem eigenen Computer verwendet werden.  
  - [ ] Das Key-Pair, welches du für die Interaktion mit deinem Server benutzen willst, solltest du auf deinem Computer 
    generieren \- **nicht** auf dem Server.  
- [ ] Deaktiviere den Passwort-Login auf dem Server  
  - [ ] Stelle sicher, dass ein Login mit einem SSH-Key erfolgreich funktioniert hat, **bevor** du den Passwort-Login 
    deaktivierst  
- [ ] Installiere den Webserver NGINX  
- [ ] Verändere die Konfiguration von NGINX, sodass eine alternative HTML-Seite als Einstiegspunkt angezeigt wird. 
  Gegebenenfalls muss hierzu NGINX neu gestartet werden  
- [ ] Konfiguriere git auf deinem V-Server so, dass dein Nutzername und deine E-Mail-Adresse hinterlegt sind. 
  Die Benutzerdaten sollten den Daten auf deinem Computer entsprechen, bzw. deckungsgleich mit deinen in GitHub 
  hinterlegten Daten sein.  
  - [ ] Um die Konfiguration für Git und GitHub vollständig abzuschließen, solltest du ein SSH-Key-Pair auf deinem 
    Server anlegen, sodass du den Public Key in GitHub hinterlegen kannst, um von deinem Server aus Repositories auf den
    Server zu pullen und mit ihnen zu interagieren.

## 2. **Hinweise**

### **Allgemeine Hinweise**

- [ ] Zusätzlich zu deinem GitHub Repository solltest du ein kurzes Loom Video (maximal 5min.) aufnehmen und 
  bereitstellen, indem du kurz deine Abgabe zeigst und vorstellst, was du getan hast \- dabei musst du nicht alle 
  Details erwähnen, jedoch sollst du auf alle relevanten Schritte kurz eingehen und diese zeigen

### **Sicherheitshinweise**

- [ ] Stelle sicher, dass ein Login mit einem SSH-Key erfolgreich funktioniert hat, **bevor** du den Passwort-Login 
  deaktivierst

### **Testing**

Bevor du dein Projekt einreichst, solltest du die folgenden Dinge sichergestellt und getestet haben:

- [ ] Ich habe die [FAQ Seite](https://developer-akademie-devsecopskurs.github.io/dso-faq-site/de/docs/projects/vserver-setup/faq) für dieses Projekt durchgelesen und alle Punkte umgesetzt  
- [ ] Es wird das bereits vorhandene Docusaurus Projekt genutzt  
- [ ] Es gibt einen Feature Branch und einen Pull Request in DEINEM Docusaurus Repo  
- [ ] Dieser Pull Request enthält eine Ordnerstruktur, die folgendermaßen aussehen sollte: 
  <span style="background-color: lightgrey;">/docs/v-server/</span> mit einer
  <span style="background-color: lightgrey;">README.md</span>   
- [ ] In dieser README.md ist deine technische Dokumentation beschrieben  
- [ ] Man kann sich mit Hilfe eines SSH-Keys auf dem Server anmelden  
- [ ] Man kann sich **nicht** mit einer Kombination aus Nutzernamen und Passwort anmelden  
  - [ ] Hierzu kann die SSH-Option <span style="background-color: lightgrey;">\-o PubKeyAuthentication=no</span> 
   hilfreich sein z.B. <span style="background-color: lightgrey;">ssh \-o PubKeyAuthentication=no \-i pfad/zum/
   private-key user@12.34.67.89</span>  
- [ ] Teste die Verfügbarkeit deines Webservers, indem du die IP-Adresse des V-Servers in deinen Browser in der 
  Adresszeile eingibst und die Eingabe bestätigst. Du solltest dann einen Willkommens-Bildschirm von NGINX angezeigt 
  bekommen  
  - [ ] Bevor du die Konfiguration anwendest, kannst du diese mithilfe von   
    <span style="background-color: lightgrey;">nginx \-t</span>  validieren (deine Konfiguration liegt unter
    <span style="background-color: lightgrey;">/etc/nginx/nginx.conf</span>)  
  - [ ] Falls du eine eigene Konfigurationsdatei für nginx hast, dann kannst du diese folgendermaßen isoliert testen:  
    <span style="background-color: lightgrey;">nginx \-t \-c pfad/zur/config</span>  
- [ ] Validiere, dass die neue Konfiguration von deinem NGINX Server angewendet wird und im Browser dementsprechend 
  deine HTML-Seite zu sehen ist

## 3. **Dokumentation**

### **Git-Repository mit README**

- [ ] Die Dokumentation soll auf Englisch geschrieben werden.  
- [ ] Achte darauf, dass du nicht sicherheitskritische Inhalte wie dein Passwort oder den Inhalt deiner SSH Keys in 
  das Repository schreibst.  
- [ ] Die README Datei sollte in Markdown Format geschrieben und ordentlich strukturiert sein  
- [ ] Eine Inhaltsangabe sollte vorhanden sein  
- [ ] Die einzelnen Schritte sollten jeweils in einer Sektion, oder ggf. auch in einem eigenen Dokument beschrieben 
  sein. Bei mehreren Dokumenten sollten diese sinnvoll miteinander verlinkt sein.  
- [ ] Diese Checkliste sollte ebenfalls als PDF im Repository enthalten sein.

Bei deiner Abgabe solltest du am besten auch die IP-Adresse deines V-Servers mit angeben, sodass die Mentoren dort auch 
die Konfiguration überprüfen können.