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
