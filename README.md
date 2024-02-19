# Workshop-Anleitung: Einführung in m5Stack

## Für Lehrende

### Ziel des Workshops:
Dieser Workshop zielt darauf ab, Lehrenden ohne Vorkenntnisse die Grundlagen der Arbeit mit m5Stack und der Programmierung mit UIFlow beizubringen.

### Vorbereitung des Workshop-Raums (Dauer: ca. 1 Stunde)
1. **Tische und Laptops aufstellen:**
   - Stellen Sie die Tische auf und platzieren Sie die Laptops.
   - Schließen Sie die Laptops an den Strom an.
   - Verbinden Sie Mäuse mit den Laptops.

2. **m5Stack vorbereiten:**
   - Schließen Sie die m5Stack-Geräte an den Strom an.
   - Überprüfen Sie, ob die Geräte grün leuchten (dies zeigt eine Verbindung mit dem WLAN an).
   - Bild von m5Stack mit grüner LED [Bild von m5Stack mit grüner LED...]

3. **Technische Einrichtung:**
   - Starten Sie den Touch-Fernseher und verbinden Sie ihn nötigenfalls.
   - Öffnen Sie auf den Laptops die Webseite [https://flow.m5stack.com/](https://flow.m5stack.com/) und wählen Sie UIFlow 1.0.
   - Sollte kein API-Schlüssel angezeigt werden, versuchen Sie, den m5Stack neu zu verbinden.
   - Klicken Sie auf das Aktualisierungssymbol, um eine Verbindung mit einem m5Stack herzustellen.
   - Bild von der UIFlow Webseite mit dem API-Schlüssel [Bild von UIFlow...]

4. **m5Stack identifizieren und zuordnen:**
   - Schreiben Sie eine Zahl oder ein Muster in der Matrix und klicken Sie auf "Run", um den entsprechenden m5Stack zu identifizieren.
   - Bringen Sie den identifizierten m5Stack zum jeweiligen Laptop.
   - Wiederholen Sie diesen Schritt für alle Teilnehmer und den Präsentator.

5. **Beispielcode auf ESP laden:**
   - Laden Sie den Beispielcode aus diesem Ordner auf den ESP des Präsentators.

### Workshop Beginn (Dauer: ca. 5-10 Minuten)
- Warten Sie, bis alle Teilnehmer eingetroffen sind.
- Stellen Sie den Ablauf vor:
  - Vorstellung der Lehrenden.
  - Abfrage der Vorkenntnisse der Teilnehmer im Bereich Programmierung.
  - Präsentation des Endergebnisses und Vorführung aller Funktionen.
  - Einführung in die Programmierung und Vorstellung eines praktischen Beispiels (z.B. Telegram Bot zur Steuerung einer Schranke).
  - Betonung der Effizienz und Nützlichkeit der Informatik.

### Einführung in UIFlow
- Erklären Sie den Aufbau der UIFlow-Oberfläche, insbesondere die Matrix auf der linken Seite und den "Run"-Button.
- Die Teilnehmer sollen ein Bild oder Smiley in der Matrix erstellen und die Farben anpassen.
- Betonen Sie, dass auf "Run" und nicht auf "Download" geklickt werden sollte.
- Überprüfen Sie, ob es bei allen Teilnehmern funktioniert.

### Aufgabe 2: Verstehen des Code-Baus und der Puzzle-Teile

1. **Zugriff auf Hardware-Komponenten:**
   - Navigieren Sie im UIFlow-Menü zum Abschnitt "Hardware" und dann zum Unterabschnitt "RGB".
   - Ziehen Sie die LED-Matrix aus dem Menü in das Arbeitsfenster.

2. **Platzierung der LED-Matrix:**
   - Ziehen Sie die LED-Matrix in das schwarze Feld. Beachten Sie, dass alles, was grau hinterlegt ist, nicht ausgeführt wird.
   - Ziehen Sie die LED-Matrix zum "Setup"-Block, um sie aktiv zu nutzen.
   - Malen Sie ein neues Bild auf der LED-Matrix.

### Aufgabe 3: Bildänderung bei Knopfdruck

1. **Ereignis für Taste A hinzufügen:**
   - Wählen Sie im UIFlow-Menü unter "Ereigniss" die Option "Taste A was Pressed".
   - Ziehen Sie diesen Block in Ihr Arbeitsfenster.

2. **LED-Matrix integrieren:**
   - Schieben Sie eine neue LED-Matrix in den "Taste A was Pressed"-Block.
   - Nun wird beim Drücken von Taste A das zweite Bild angezeigt.

### Aufgabe 4: Umschalten zwischen Bildern mit Variablen und Logik

1. **Variable erstellen:**
   - Gehen Sie zu "Variablen" und wählen Sie "Erzeuge Variable", benennen Sie diese Variable als "status".

2. **Variable initialisieren:**
   - Wählen Sie "Setze status auf" und initialisieren Sie die Variable mit 0 oder einem anderen Startwert und fügen sie ihn an "Setup" an.

3. **Logische Abfrage hinzufügen:**
   - Verwenden Sie aus dem "Logik"-Menü den Block "wenn ... dann ... sonst ..." für die Entscheidungsfindung.
   - Fügen Sie aus demselben Menü den Vergleichsblock "... = ..." hinzu, um zu überprüfen, welches Bild zuletzt angezeigt wurde.

4. **Bedingungen festlegen:**
   - Setzen Sie "status" in einen Vergleich ein, um zu entscheiden, welches Bild angezeigt werden soll, fügen sie in die andere seite eine Zahl aus Mathe ein.
   - Fügen Sie unter "führe aus" und "sonst" die entsprechenden LED-Matrix-Blöcke ein, um die Bilder zu wechseln.

5. **Status aktualisieren:**
   - Nach dem Wechsel des Bildes aktualisieren Sie den "status" mit dem neuen Wert, um das zuletzt angezeigte Bild zu speichern, also aus "Variablen" das "setze status auf".

### Aufgabe 5: Hinzufügen eines dritten Bildschirms und Durchführung einer Rotation mit Tastendrücken

In dieser Aufgabe werden die Teilnehmer lernen, wie sie einen dritten Bildschirm in ihre bestehende Schaltung integrieren und eine Rotation zwischen den drei Bildschirmen durch Tastendrücke ermöglichen können. Dies erfordert eine Erweiterung der logischen Abfrage, um eine zusätzliche Bedingung für das dritte Bild zu berücksichtigen.

#### Schritt-für-Schritt-Anleitung

1. **Erweiterung der logischen Abfrage:**
   - Gehen Sie zu Ihrem bestehenden "wenn ... dann ... sonst ..." Block.
   - Klicken Sie auf das Zahnrad-Symbol am Block, um die Blockstruktur anzupassen.
   - Fügen Sie ein "sonst wenn" hinzu, um eine weitere Bedingung für das dritte Bild zu schaffen.

2. **Konfiguration der neuen Bedingung:**
   - Stellen Sie innerhalb des "sonst wenn" Blocks die Bedingung ein, die überprüft, welches Bild zuletzt angezeigt wurde und ob nun das dritte Bild angezeigt werden soll.
   - Sie können dies tun, indem Sie die Variable "status" mit einem neuen Wert vergleichen, der dem dritten Bild zugeordnet ist (zum Beispiel "2" für das dritte Bild).

3. **Hinzufügen des dritten Bildschirms:**
   - Platzieren Sie innerhalb des "sonst wenn" Blocks einen weiteren LED-Matrix-Block, um das dritte Bild zu definieren und anzuzeigen.

4. **Aktualisierung der Statusvariable:**
   - Nachdem das dritte Bild angezeigt wurde, müssen Sie sicherstellen, dass der "status" entsprechend aktualisiert wird, um den aktuellen Zustand zu reflektieren.
   - Fügen Sie nach dem Anzeigen des dritten Bildes einen Block hinzu, um "status" auf den nächsten Wert zu setzen, der den Beginn der Rotation zurück zum ersten Bild signalisiert.

5. **Testen und Debugging:**
   - Geben Sie den Teilnehmern Zeit, um diese Aufgabe durchzuführen, und bieten Sie Unterstützung an, wo sie benötigt wird.
   - Es ist wichtig, dass die Teilnehmer verstehen, wie die logische Struktur ihrer Programme funktioniert und wie sie durch die verschiedenen Zustände ihrer Programme navigieren können.

#### Beispiel für die logische Struktur:

- Wenn "status = 0", dann zeige Bild 1 und setze "status" auf 1.
- Sonst wenn "status = 1", dann zeige Bild 2 und setze "status" auf 2.
- Sonst wenn "status = 2", dann zeige Bild 3 und setze "status" auf 0 (oder einen anderen Anfangswert, um die Rotation fortzusetzen).

Durch diese Übung lernen die Teilnehmer, wie sie komplexe logische Strukturen in ihren Programmen einbauen und nutzen können, um interaktive und dynamische Projekte zu erstellen. Es hilft auch, ein tieferes Verständnis für die Verwendung von Variablen, Bedingungen und Aktionen in der Programmierung zu entwickeln.

Diese Schritte führen die Teilnehmer durch fortgeschrittene Konzepte der Ereignisbehandlung, Zustandsverwaltung und Ablaufsteuerung mit dem m5Stack und UIFlow. Durch das Trennen von Logik und Aktionen sowie das Einführen von Zeitsteuerung und Zustandsänderungen durch externe Ereignisse erhalten die Teilnehmer ein tieferes Verständnis für die Erstellung von interaktiven und reaktiven Programmen.

### Aufgabe 6: Logik und Aktion trennen

1. **Einführung in Ereignisschleifen:**
   - Unter "Ereignisse" finden Sie die Option für eine kontinuierliche Schleife. Erklären Sie, dass in diese Schleife die gesamte logische Abfolge integriert wird.

2. **Aufteilung der Logik und Aktion:**
   - Duplizieren Sie den logischen Block (Rechtsklick > Duplizieren) und platzieren Sie eine Kopie in die Schleife.
   - Entfernen Sie in der Schleifen-Version die Aktion des Bildwechsels und behalten Sie nur die logische Zustandsüberprüfung.
   - Im Ereignisblock (z.B. Button-Druck) entfernen Sie die Logik und behalten nur die Aktion des Bildwechsels und das Setzen der Variablen.

3. **Zweck der Trennung:**
   - Erklären Sie, dass durch diese Trennung die Möglichkeit geschaffen wird, Zustandsänderungen auch durch andere Ereignisse einzuleiten, was die Flexibilität des Programms erhöht.

### Aufgabe 7: Optimierung der LED-Matrix-Anzeige

1. **Vermeidung ständiger Aktualisierungen:**
   - Führen Sie eine neue Variable ein, z.B. "geändert", um zu verfolgen, ob eine Änderung stattgefunden hat.

2. **Logik für einmalige Aktualisierung:**
   - Setzen Sie "geändert" auf 1 bei jedem Button-Druck und auf 0 nach der Auswertung der logischen Abfrage in der Schleife.
   - Fügen Sie eine Bedingung hinzu, die überprüft, ob "geändert = 1" ist, und führen Sie dann den logischen Block aus, um die LED-Matrix nur bei tatsächlichen Änderungen zu aktualisieren.

### Aufgabe 8: Implementierung einer automatischen Notabschaltung

1. **Timer zur Zeitüberwachung:**
   - Erstellen Sie einen Timer (unter "Ereignisse" > "timer Callback timer1"), der nicht direkt mit anderen Blöcken verbunden ist.
   - Setzen Sie im Timer-Callback "status" auf einen Fehlerzustand, z.B. 10.

2. **Timer starten:**
   - Starten Sie den Timer mit "Ereignis" > "Start timer1 period 15000 ms mode oneshot" in den Zuständen, die eine Aktion ausführen (z.B. Status 2 und 3).

3. **Behandlung des Fehlerzustands:**
   - Die Teilnehmer sollen nun selbst den Fehlerzustand (z.B. Status 10) implementieren und sicherstellen, dass "geändert" korrekt gesetzt wird, um die Anzeige zu aktualisieren.

### PAUSE:

### Aufgabe 9: Handy verbinden

1. **Fernbedienung+ nutzen:**
   - Wählen Sie in UIFlow die Option "Fernbedienung+" aus.
   - Ziehen Sie das Feld [123] auf das angezeigte Handy-Interface, um ein Anzeigefeld zu erstellen.

2. **QR-Code generieren und scannen:**
   - Durch das Klicken auf "Run" wird neuer Code erzeugt, der einen QR-Code enthält.
   - Dieser QR-Code kann gescannt oder über einen Klick kopiert werden, um die Verbindung mit einem Handy oder PC herzustellen.

3. **Anzeige von Daten:**
   - Ändern Sie den angezeigten Text von [123] auf die Variable "status", um den Status über die Fernbedienung anzuzeigen.
   - Testen Sie die Aktualisierung auf dem Handy oder PC. Beachten Sie, dass die Webseite sich nur alle 3 Sekunden aktualisiert.

### Aufgabe 10: Der Wasser Sensor

1. **Wasser Sensor hinzufügen:**
   - Klicken Sie unter "Units" auf das weiße Pluszeichen (+) und suchen Sie nach "Wa" für den Wassersensor ("WATERING").
   - Fügen Sie den Wassersensor zur Liste Ihrer verfügbaren Aktionen hinzu.

2. **Feuchtigkeitswert lesen:**
   - Ziehen Sie den Block "get Watering_0 adc value" in Ihr Arbeitsfenster, um den aktuellen Feuchtigkeitswert zu messen.
   - Platzieren Sie diesen Block, um den Wert auf der Fernbedienung+ anzuzeigen.

3. **Schwellwerte festlegen:**
   - Notieren Sie den ADC-Wert bei keiner Berührung und ziehen Sie 50 ab, um Schwankungen auszugleichen.
   - Halten Sie den Sensor locker, um einen feuchten Wert zu messen, und ziehen Sie 50 von diesem Wert ab.
   - (optional)Umschließen Sie den Sensor fest, um einen sehr feuchten Wert zu messen, und addieren Sie auch hier 50.

### Aufgabe 11: Auswertung der Feuchtigkeit und Setzen des Status

1. **Bedingungen für Feuchtigkeitswerte festlegen:**
   - Fügen Sie einen "wenn ... dann ... sonst wenn ... sonst"-Block ein.
   - Für die erste Bedingung verwenden Sie einen Vergleichsoperator (>) und vergleichen Sie den ADC-Wert des Wassersensors ("get Watering_0 adc value") mit dem niedrigsten aufgeschriebenen Wert für "nichts Wert".

2. **Erstellung der zweiten Bedingung:**
   - Die Teilnehmer sollen nun basierend auf den zuvor aufgeschriebenen Werten die zweite Bedingung selbst erstellen.
   - Diese Bedingung überprüft, ob der Feuchtigkeitswert über dem mittleren Wert liegt (zweiter Wert), und setzt den Status entsprechend.

3. **Aktualisierung der "geändert"-Variable:**
   - Um sicherzustellen, dass Änderungen angezeigt werden, setzen Sie die Variable "geändert" auf 1, jedes Mal wenn der Status geändert wird.

### Aufgabe 12: Status nur bei Änderung setzen

1. **Einführung einer neuen Variable:**
   - Erstellen Sie eine Variable, z.B. "letzterStatus", um den vorherigen Statuswert zu speichern.

2. **Überprüfung auf Statusänderung:**
   - Implementieren Sie eine Bedingung, die überprüft, ob der aktuelle Status sich vom "letzterStatus" unterscheidet.
   - Wenn sich der Status geändert hat ("status != letzterStatus"), dann:
     - Setzen Sie "letzterStatus" auf den aktuellen "status".
     - Setzen Sie "geändert" auf 1, um anzuzeigen, dass eine Aktualisierung erforderlich ist.
   - Entfernen Sie die Aktualisierung der "geändert"-Variable aus allen anderen Bedingungen, damit sie nur innerhalb dieser neuen Logik vorgenommen wird.

Diese Aufgaben führen die Teilnehmer durch den Testprozess ihrer bisherigen Arbeit und leiten sie dann zu einem praktischen Experiment mit Wasser und dem Wassersensor. Es geht darum, das Verständnis und die Anwendung der gelernten Konzepte in einem realen Kontext zu überprüfen und zu festigen.

### Aufgabe 13: Testen der gesamten Konfiguration

1. **Überprüfen der Funktionalitäten:**
   - Stellen Sie sicher, dass die LED-Matrix sich ändert, wenn der Sensor umschlossen wird.
   - Überprüfen Sie, ob die automatische Notabschaltung aktiviert wird, wenn der Sensor zu lange umschlossen bleibt.
   - Testen Sie, ob der Notaus-Zustand bestehen bleibt, bis eine Taste gedrückt wird, um ihn zurückzusetzen.

2. **Permanente Notabschaltung implementieren:**
   - Führen Sie eine Bedingung ein, die verhindert, dass der Status geändert wird, wenn der aktuelle Status gleich 10 ist. Dies soll sicherstellen, dass der Notaus-Zustand bestehen bleibt, bis er manuell zurückgesetzt wird.
   - Die Teilnehmer sollen diese Bedingung eigenständig implementieren, ähnlich dem Vorgehen bei der "geändert"-Variable, ohne jedoch eine neue Variable einzuführen.

### Aufgabe 14: Praktisches Experiment mit Wasser
Diese logik ist invertiert, damit es nicht zu unfällen kommt

1. **Vorbereitung des Experiments:**
   - Jede Gruppe erhält ein leeres Glas, in das die Schläuche des Wassersensors und der Pumpe gelegt werden können. Es sollte beachtet werden, dass aus den Schläuchen zunächst etwas Wasser austreten kann.

2. **Programmierung der Pumpe:**
   - Programmieren Sie die Pumpe so, dass sie sich ausschaltet (Status Off), wenn der Status auf 1 oder 10 gesetzt ist. Dies verhindert das Pumpen von Wasser in unerwünschten Zuständen.
   - Stellen Sie die Pumpe so ein, dass sie eingeschaltet wird (Status On), wenn der Status auf 2 oder 3 gesetzt ist. Dies ermöglicht das Pumpen von Wasser, basierend auf den Feuchtigkeitsmesswerten des Sensors.

3. **Durchführung des Experiments:**
   - Testen Sie, ob die Pumpe wie erwartet reagiert. Wenn ja, erhalten die Teilnehmer ein Wasserglas, um das Wasser von einem Glas in ein anderes zu pumpen.

Durch das Testen und das praktische Experiment mit dem Wasser lernen die Teilnehmer nicht nur die theoretischen Grundlagen, sondern auch, wie diese in praktischen Anwendungen umgesetzt werden können. Es demonstriert die Wichtigkeit von genauen Tests und Anpassungen in der Entwicklung von Projekten, die auf physischen Interaktionen basieren.

Diese Aufgaben ermutigen die Teilnehmer, ihre Projekte weiter zu verfeinern, indem sie Anpassungen basierend auf realen Bedingungen vornehmen und zusätzliche Funktionalitäten wie die Steuerung der Pumpgeschwindigkeit implementieren.

### Aufgabe 15: Anpassungen und Experimente

1. **Bildanpassungen:**
   - Die Teilnehmer erhalten Zeit, um die Bilder auf der LED-Matrix nach Belieben zu ändern. Sie können kreativ sein und Designs erstellen, die ihrer Meinung nach die verschiedenen Feuchtigkeitszustände am besten darstellen.

2. **Anpassung der ADC-Werte:**
   - Falls gewünscht, können die Teilnehmer die ADC-Schwellwerte anpassen, um sie an die Feuchtigkeitsbedingungen einer echten Pflanze anzupassen. Sie sollten bedenken, dass eine nasse Pflanze länger nass bleibt.

3. **Experimentieren mit dem System:**
   - Die Teilnehmer können mit der Wasserpumpe experimentieren, indem sie den Notaus-Zustand testen oder die Zeit bis zur automatischen Abschaltung anpassen, um zu sehen, wie das System auf verschiedene Bedingungen reagiert.

### Aufgabe 16: Anpassung von Status 2 für langsamere Pumpgeschwindigkeit

1. **Einrichtung eines Timers:**
   - Erstellen Sie einen neuen Timer (timer_2) und setzen Sie ihn auf periodisch mit einem Intervall von 50ms. Dieser Timer wird verwendet, um die Pumpe in kurzen Intervallen ein- und auszuschalten, um eine halbe Geschwindigkeit zu simulieren.

2. **Programmierung des Callbacks:**
   - Ziehen Sie den Callback für timer_2 in Ihr Arbeitsfenster und erstellen Sie darin eine Bedingung, die prüft, ob die Pumpe ein- oder ausgeschaltet werden soll. Verwenden Sie eine Variable, um den Zustand (ein/aus) bei jedem Timer-Intervall zu wechseln.

3. **Anpassung beim Statuswechsel:**
   - Um sicherzustellen, dass die Pumpe nicht weiterläuft, wenn der Status sich ändert, fügen Sie die Aktion "Stop timer_2" in die Bedingung ein, die überprüft, ob sich der Status geändert hat. Dies stoppt die Pumpe, wenn der Status nicht mehr 2 ist.

4. **Testen der Anpassungen:**
   - Nachdem die Teilnehmer die Timer-Logik implementiert haben, sollten sie das System testen, um sicherzustellen, dass die Pumpe bei Status 2 mit der gewünschten, halbierten Geschwindigkeit läuft und dass der Timer korrekt gestoppt wird, wenn der Status wechselt.

Durch diese Anpassungen und Tests lernen die Teilnehmer, wie man ein System feinabstimmt und auf spezifische Anforderungen reagiert. Sie erfahren auch, wie wichtig es ist, die Funktionalität ihres Systems unter verschiedenen Bedingungen zu überprüfen und anzupassen, um eine optimale Leistung zu erzielen.

Falls zusätzliche Zeit zur Verfügung steht, können diese optionalen Aufgaben den Teilnehmern helfen, ihr Verständnis und ihre Fähigkeiten im Umgang mit dem m5Stack und UIFlow weiter zu vertiefen. Diese Aufgaben erweitern die Interaktivität und Funktionalität ihres Projekts und bieten Möglichkeiten für kreativen Ausdruck und technische Verfeinerung.

### Weboberfläche erweitern

1. **Status als Text anzeigen:**
   - Integrieren Sie ein Textfeld auf der Weboberfläche, das den aktuellen Status als lesbaren Text darstellt, z.B. "Trocken", "Feucht", "Nass", "Notaus".

2. **Button zum Zurücksetzen des Fehlers:**
   - Fügen Sie einen Button hinzu, mit dem der Nutzer einen Fehlerzustand (z.B. den Notaus) zurücksetzen kann, um die normale Funktionsweise ohne physischen Eingriff am m5Stack wiederherzustellen.

3. **Zeitanzeige für aktuellen Status:**
   - Implementieren Sie eine Funktionalität, die anzeigt, wie lange der aktuelle Status bereits aktiv ist. Dies kann durch eine einfache Zeitstempel-Logik erreicht werden, die bei jeder Statusänderung zurückgesetzt wird.

4. **(Experten) Wassergeschwindigkeit mit Slider einstellen:**
   - Für fortgeschrittene Teilnehmer kann eine Option hinzugefügt werden, um die Geschwindigkeit der Wasserpumpe für Status 2 über einen Slider auf der Weboberfläche einzustellen. Dies erfordert eine Anpassung der Timer-Logik und eventuell die Implementierung einer dynamischen Steuerung der Ein-/Ausschaltintervalle basierend auf dem Slider-Wert.

### LED-Matrix Animationen

1. **Animationen erstellen:**
   - Nutzen Sie Timer, um verschiedene Bilder oder Muster auf der LED-Matrix in einer Animation abzuspielen. Dies kann dazu dienen, den aktuellen Feuchtigkeitszustand oder den Betriebsmodus auf eine visuell ansprechende Weise darzustellen.

### Weitere einfache Optionen

1. **Akustische Signale:**
   - Integrieren Sie akustische Signale für bestimmte Ereignisse oder Statusänderungen, um eine zusätzliche Feedbackebene zu bieten.

2. **Farbänderungen auf der LED-Matrix:**
   - Verwenden Sie Farbänderungen auf der LED-Matrix, um unterschiedliche Zustände oder Warnungen zu signalisieren, z.B. könnte Rot einen Notaus-Zustand darstellen.

3. **Datenspeicherung:**
   - Implementieren Sie eine einfache Datenspeicherung oder -protokollierung für Ereignisse wie Statusänderungen, Notaus-Aktivierungen oder Feuchtigkeitswerte. Dies kann für spätere Analysen oder zur Überwachung der Pflanzengesundheit nützlich sein.

Durch die Arbeit an diesen optionalen Aufgaben können die Teilnehmer nicht nur ihr Projekt erweitern, sondern auch wertvolle Erfahrungen in der Entwicklung von interaktiven und benutzerfreundlichen Anwendungen sammeln.