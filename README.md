<h1>
Arduino-Tutorial und Nixie-Clock
</h1>

<h2>
<a id="Inh"> Inhalt </a>
</h2>

<ul>
<li><a href="#lvl1"> Wie funktioniert ein Arduino?</a></li>
<li><a href="#lvl2"> Nixie-Tube Uhr</a></li>
<li><a href="#lvl3"> Bens Nixie Tube Uhr</a></li>
<li><a href="#lvl4"> Dokumentation </a></li>
<li><a href="#Quell"> Quellen</a></li>
</ul>

<p>
Dies ist eine Github Dokumentation von unserem Fortschritt in der Arduino Programmierung.
</p>

<h2>
Wie funktioniert ein Arduino?Dokumentation</h2>

<p>
Ein Arduino ist ein Mikrocontroller von der gleichnahmigen Firma, die 2005 gegründet wurde.
Der Arduino funktioniert, indem man einen Code auf den Controller lädt. Außerdem muss man, um etwas zu bewirken in die Steckplätze etwas anschließen.
Diese können je nach dem hochgeladenen Code entweder an 0V oder 5V angelegt werden. Außerdem gibt es besondere Pins, die Informationen von anderen Modulen bekommen und je nach Code ausgewertet werden können.
Durch dieses System ist qusi eine unendliche Vielfältigkeit gewährleistet, die nur durch die eigenen Programmierkenntnisse begrenzt wird.
Diese Kenntnisse können glücklicherweise durch die extrem große Community des Arduinos einfach erlernt und verbessert werden.
</p>
<p>
Den erwähnten Code kann man in der Entwicklungsumgebung, die man über die Webseite von Arduino kostenlos herunterladen kann, geschrieben werden.
</p>

<h2>
Nixie-Tube Uhr:
</h2>
<p>
Nixie Tubes sind Röhren die bis in die Siebziger benutzt wurden um Informationen anzuzeigen. Sie wurden später durch die Displays abgelöst.
Nixie Tubes sind mit einem Edelgas gefüllt und enthalten leitende Ziffern, die die Anode darstellen. Als Kathode wird ein Gitter vor oder hinter den Ziffern benutzt.
Setzt man nun eine Spannung an eine Ziffer und die Kathode. Fängt die Ziffer an zu glühen und leuchtet so auf. Die angelegte Spannung muss dafür zwischen 150 und 190V liegen.
Es gibt Röhren die alle mögliche Ziffern anzeigen können also kann man Nixie Tubes für alle mögliche Displays benutzen. 
</p>
<h2>
Bens Nixie Tube Uhr:
</h2>
<p>
Ich habe vor einiger Zeit eine solche Uhr gesehen und fand sie vom Aussehen sehr ansprechend.
Da eine fertige Uhr circa 500€ kostet war das Besitzen einer solchen Uhr bislang utopisch.
Allerdings habe ich bei der Suche nach einem neuen Informatik Projekt diese Uhr wieder gesehen und dachte dass man diese bestimmt auch durch einen Arduino steuern kann.
</p>
Hier ergaben sich mir allerdings mehrere Probleme:
1. Die Röhren brauchen zum Leuchten eine Spannung von mindestend 150V. Allerdings kann der Arduino nur höchstens 5V ausgeben.
Dieses Problem wird gelöst, in dem man einen Mikrocontroller zwischen den Arduino und die Röhren schaltet. Er wirkt als ein Transistor nur mit mehreren Ausgängen. Um dem Mikrocontroller anzusteuern muss man einen 4-stelligen Binärcode benutzen. Dieser kommt durch entweder eine Eins (in diesem Fall wird 5V an das Kabel angelegt) oder eine Null (0V) zustande die durch vier verschiedene Kabel gesendet werden. Je nachdem wo die 5V angelegt werden, schaltet also der Mikrocontroller die verschiedenen Ziffern. 
2. Man darf höchstens 190V anlegen, ansonsten brennen die Röhren durch.
Dies bedeutet, dass man nicht direkt die Steckdosenspannung benutzen kann.
Dies wird durch einen Voltwandler gelöst. Er liefert die richtige Spannung für die Röhren. Man kann sogar alle Röhren an eine Spannung anlegen.
3. Die 
Wegen Zeitmangel und Lieferengpässen wird dieser Teil nur theoretisch





Dokumentation:
Nachdem wir uns für die Arduiono Programmierung entschieden haben, haben wir ein Tutorial für die Basics der Arduino Programmierung bearbeitet, da wir bisher keine Vorkenntnisse hatten.
Dieses Tutorial ist auf mymakerstuff.de zu finden. 

2.3.2017 
Hier haben wir angefangen die Arduiono Programmiersprache zu lernen, indem wir eine LED zum leuchten gebracht haben.
Hierzu haben wir den wir den Beispielcode von mymakerstuff.de verwendet und unseren Ansprüchen nach verändert. 
Im Tutorial haben wir eine LED zum Blinken gebracht, indem wir den Beispielsketch Blink aus dem Arduino Programm benutzt haben.
Um die Funktionsweise besser zu verstehen, haben wir ein SOS-Signal programmiert. 

Hier Video einfügen:

Nachdem wir eine einfache LED zum Blinken gebracht hatten, haben wir eine Ampelschaltung programmiert. 
Hierzu haben wir eine rote, gelbe und grüne LED so programmiert, dass sie wie eine Ampelschaltung im realen Leben funktionieren.

Hier Video und Code:

9.3.2017
An diesem Tag haben wir angefangen einen Taster mit in die Schaltung einzubauen. Auch hierzu haben wir das Tutorial von mymakerstuff.de benutzt.
Je nachdem ob der Taster gedrückt oder nicht gedrückt ist, ist die LED an oder aus. 

Hier Video und Code:

Als nächstes haben wir vier LED's angeschlossen und diese so programmiert, dass man mit dem Taster die LED's durchschalten kann. 
Hier ist uns aufgefallen, dass ein Taster prellen kann, das bedeutet dass innerhalb des Tasters durch Wackelkontakte missverständliche Signale an den Arduino geschickt werden.
Dies konnte durch Pausen zwischen der Bedienung des Tasters kontrolliert werden. 

Hier Video: 

15.3.2017
Hier hat Ben angefangen seine Nixie Tube Uhr zu Programmieren. In dieser Stunde hat er sich einen Überblick verschafft was dazu nötig ist.

16.3.2017 
In dieser Stunde hat Ben angefangen Die Binärcodes für die Mikrocontroller zu programmieren. 


