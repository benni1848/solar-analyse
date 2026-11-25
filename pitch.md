# Pitch: Solar-Potenzial-Analyse
*Aufgabe #3 – KI als Toolbox · Architekturwerkzeuge IV · Sprechzeit ca. 2–3 Minuten*

Jede Folie hat Stichpunkte für die Folie und darunter (als Zitat) den Sprechtext.

## Folie 1 – Titel
**Solar-Potenzial-Analyse**
*Wie viel Sonne steckt in unserem Entwurf?*

> „Jede Dachfläche und jede Fassade ist ein potenzielles Kraftwerk. Wir haben ein Tool gebaut, das schon in der ersten Entwurfsskizze zeigt, wie viel Strom darin steckt.“

## Folie 2 – Grundlage
- Klimagerechtes Bauen ist inzwischen Pflicht und keine Kür mehr.
- PV wird häufig erst in der Fachplanung berücksichtigt, wenn die Form schon feststeht.

> „Die Idee kam aus unseren eigenen Entwürfen. Wir drehen Baukörper, ändern Dachneigungen und diskutieren Fassaden, wissen aber nie, was das energetisch bedeutet. Mit Sonnenstand und Ausrichtung haben wir uns schon in Gebäudetechnik und Bauphysik beschäftigt. Uns fehlte aber ein Werkzeug, das dieses Wissen direkt im Entwurf nutzbar macht.“

## Folie 3 – Problem
- Frage im Entwurf: Lohnt sich PV auf dieser Fläche?
- Fachsoftware wie PVSyst oder PV*SOL ist für frühe Phasen zu komplex.
- Die Faustformel „Süddach, 30°“ hilft bei Fassaden und Ost-West-Dächern nicht weiter.

> „Das konkrete Problem: In der frühen Phase gibt es keine schnelle, verständliche Antwort darauf, was eine bestimmte Fläche an Solarertrag bringt. Fachsoftware ist aufwendig und für Planer:innen gedacht, nicht für Entwerfende. Deshalb wird die Entscheidung oft aus dem Bauch heraus getroffen oder auf später verschoben.“

## Folie 4 – Lösung
- Web-App direkt im Browser, ohne Installation und ohne Account
- Flächen anlegen: Größe, Neigung, Ausrichtung, Verschattung
- Live-Ergebnis: Ertrag, kWp, CO₂-Einsparung, Ersparnis, Amortisation
- Ausrichtungskarte, Sonnenbahn, Monatsertrag, CSV-Export

> „Unsere Lösung ist eine Web-App. Man wählt einen Standort, zum Beispiel Münster, und legt beliebig viele Flächen an: Dächer, Fassaden, Vordächer. Jede Änderung an Neigung oder Ausrichtung schlägt sofort auf Ertrag, CO₂-Einsparung und Amortisation durch. Das Herzstück ist die Ausrichtungskarte. Sie zeigt für den Standort alle Kombinationen aus Neigung und Himmelsrichtung, das Optimum und, wo unsere eigenen Flächen liegen. So sieht man auf einen Blick, dass ein Norddach mit 35° noch rund 60 % des Optimums erreicht und eine Westfassade etwa 55 %. Solche Zahlen verändern Entwurfsentscheidungen.“

## Folie 5 – Methode (wie funktioniert das Tool?)
- Langjährige Monatsmittel der Globalstrahlung je Standort
- Sonnenstand für einen typischen Tag pro Monat, in Viertelstunden-Schritten
- Aufteilung in Direkt- und Diffusstrahlung, Umrechnung auf die geneigte Fläche
- Ertrag = Einstrahlung × Fläche × Wirkungsgrad × (1 – Verluste) × (1 – Verschattung)

> „Hinter der Oberfläche steckt ein anerkanntes Rechenverfahren. Wir nehmen die durchschnittliche Sonneneinstrahlung des Standorts, berechnen den Sonnenstand im Tagesverlauf und rechnen die Strahlung auf jede beliebig geneigte und gedrehte Fläche um. Direkte Sonne, diffuses Himmelslicht und Reflexion vom Boden werden dabei getrennt betrachtet. Zur Kontrolle: Für ein Münsteraner Süddach mit 35° liefert das Tool etwa 940 Kilowattstunden pro Kilowatt-Peak. Das passt zu den Referenzwerten.“

## Folie 6 – Demovideo
*(Bildschirmaufnahme, ca. 30–45 s)*
1. Standardprojekt in Münster: Süddach, Norddach, Westfassade
2. Norddach langsam auf Süd drehen, Kennzahlen und Punkt auf der Karte wandern mit
3. Neigung der Fassade von 90° auf 60° ziehen
4. Standort auf Freiburg umstellen, alles rechnet neu
5. Sonnenbahn zeigen, CSV exportieren

> „Im Video seht ihr, wie das Tool im Entwurf funktioniert: Wir drehen eine Dachfläche, ändern die Neigung, wechseln den Standort, und alles aktualisiert sich in Echtzeit.“

## Folie 7 – Prozess (Vibe-Coding)
- Idee aus der Beispielliste, eingegrenzt auf die Frage „Was braucht man im Entwurf?“
- Prototyp im Dialog mit einem LLM: erst Konzept und Rechenmodell, dann Oberfläche
- Iterationen: Plausibilitätsprüfung der Ergebnisse, Layout fürs Handy, Darstellung der Karte
- Veröffentlichung über GitHub Pages

> „Wir haben das Tool komplett per Vibe-Coding entwickelt. Zuerst haben wir mit der KI geklärt, was das Tool können soll und welches Rechenmodell sinnvoll ist. Danach entstand der Prototyp, den wir Schritt für Schritt verbessert haben. Wichtig war uns, die Ergebnisse nicht blind zu übernehmen. Wir haben sie gegen bekannte Referenzwerte geprüft. Außerdem haben wir Darstellungsfehler korrigiert und das Layout für das Smartphone angepasst. Programmiert haben wir dabei selbst kaum. Unsere Arbeit war, die richtigen Fragen zu stellen und die Antworten fachlich zu bewerten.“

## Folie 8 – Reflexion
**Was gut funktioniert hat**
- Vom Konzept zum funktionierenden Prototyp in sehr kurzer Zeit
- Fachwissen aus dem Studium ließ sich direkt in Anforderungen übersetzen
- Das Ergebnis ist sofort nutzbar und teilbar (ein Link reicht)

**Grenzen**
- Verschattung durch Nachbarbebauung nur als pauschaler Abschlag, kein 3D-Modell
- Monatsmittel statt stündlicher Wetterdaten, Klimawerte gerundet
- Ohne Fachwissen ist schwer zu prüfen, ob die KI richtig rechnet
- Abschätzung für den Entwurf, kein Ersatz für die Fachplanung

> „Vibe-Coding hat uns überrascht. Ein Tool, für das wir früher Wochen gebraucht hätten, stand nach wenigen Stunden. Die Grenze liegt aber nicht beim Programmieren, sondern beim Verstehen: Die KI liefert immer ein Ergebnis, auch wenn es falsch ist. Wir mussten wissen, welche Zahlen plausibel sind. Inhaltlich fehlt vor allem die echte Verschattung durch Nachbargebäude. Der nächste Schritt wäre eine Anbindung an ein 3D-Modell, zum Beispiel über Rhino und Grasshopper.“

## Folie 9 – Abschluss
> „Unser Fazit: Die Sonne sollte nicht erst in der Fachplanung mitreden, sondern schon in der ersten Skizze. Mit der Solar-Potenzial-Analyse geht das in Sekunden. Danke!“

*(Link zur App + QR-Code auf die Folie)*

