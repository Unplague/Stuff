# Reverse Plague - Intro

## Start
- Es gibt schon mehrere Infektionsherde (u.a. China)
- Weitere Modi (unranked):
    - Selbstgewähltes/random Startland
    - Ausgehend von aktueller Situation

## Ziel
- Globale Eindämmung des Virus (Start in China)
    - Verbreitung
        - Nationale Verbreitung
        - International durch Reiseverkehr
        - Random durch Events in einzelnen Ländern 
    - Effekt
        - Sterblichkeitsrate -> Rate der Neuinfektionen zu einem Zeitpunkt darf nicht höher als X sein
        - Wenn größer als X haben wir eine bestimmte, hohe Sterblichkeitsrate
        - Wenn weniger als X ist die Sterblichkeitsrate gering
        - Keine Heilung (um es simpler zu halten)

- Maßnahmen (s.u.) können mit Entscheidungsressource gekauft werden
    - Geld / Toilet-Paper-Points (Global), Daily Income
    - Zufriedenheit (Lokal), Start bei hohem Wert ~100%, sinkt bei größerer Anzahl an Inifizirten / Toten
- Auflärung kann lokal steigen
    -  Maßnahmen haben weniger Einfluss auf Zufriedenheit

## Maßnahmenkategorien
- Verschiedene Stufen der Aufklärung (kostet Geld, wenig Einfluss auf Zufriedenheit)
- Härtere Maßnahmen / Einschränkung des Alltags (kostet kein/wenig Geld, senkt  die Zufriedenheit {abhängig von Aufklärung})
- Super-Maßnahmen wie Medikamente (Sehr teuer, ggf. mit Ladezeit oder Lotterieeffekt)

## Aktionen (Actions)
- Rundenbasiert (1 Woche)

## Events
Mögliche Vorkommen die nacheinander überall auf der Welt auftreten und auf die entsprechende reagiert werden muss.
- werden vorher angekündigt sodass der Spieler Gegenmaßnahmen treffen kann
- Maßnahmen vermindern die Auswirkungen von Events (zB Ausgangssperre gegen Straßenfest)
- Kann positiv und negativ sein
- Positive Events sind zufällige Maßnahmen for free (zB 7 Tage Regenwetter, positive Mutationen)

### Beispiel Events

- Ausbruch in Region (ggf. höhere Wahrscheinlichkeit bei Nachbarländern)
- Möglicher Impfstoff gefunden

## Ende/Erfolg
- Leaderboard - Zeit und Anzahl Tote bis x% der Weltbevölkerung infiziert sind und Zufriedenheit als "nice to know"
- Kurve anzeigen
- Spawn Duration


## Aufgabenteilung
- Ralf: PM
- Ferdinand (Amuria): Spielmechanik, Balancing
- Kim:
- Chris: UI Design
- Roland (droland): Frontend
- Nils: Frontend
- Felix (citruz): Modellierung/Backend
- Gregor (grseewal): Backend
- Florian (TeamSpeakUser): Backend
- Tim (?): Schnittstelle Backend Frontend

## Infrastruktur
- Github
- Netlify? / AWS S3


## Linklist
| Name             | Link                                                                                 |
|------------------|--------------------------------------------------------------------------------------|
| Mockup           | https://docs.google.com/drawings/d/1KYPcuL2wnnnaGa04FAf9tzva3iLohAso0FPs1zivTIc/edit |
| Idee Deutschland | https://docs.google.com/document/d/1U8duMaeLdpArmTdRBQy-9LQa6ZsFhVwMynQHM4m76s8/edit |
| Devpost | https://devpost.com/software/coronafighter                                                             |
| GitHub | https://github.com/Unplague |
| Prototype | http://unplague.de/ |
| Youtube | https://www.youtube.com/watch?v=5yFiKWATnWE |

# MVP

## Vereinfachende Annahmen
- Weltbevölkerung ist über Regionen gleich verteilt
- keine lokalen Events
- keine Randomisierung
- kein perfektes Balancing

## Start
- Information über das Ziel: Halte das Level der Infizierten möglichst lange unter 70% (Hinweis: Irgendwann wirst Du 70% erreichen - das ist unvermeidlich)
- Es gibt 3 fixe Infektionsherde (unterschiedlich stark ausgeprägt)

## Stats: Auswirkungen der Maßnahmen / Events auf die Stats
- Zufriedenheit (je Region)
- Infektionsrate (je Region und aggregiert für die Welt)
- Anzahl der Toten
- Entscheidungsressource (TPP / Money) (global), die SpielerIn jede Runde erhält (fix)

## Oberfläche
- Weltkarte mit einzelnen Regionen (Ebene: Zentraleuropa, Osteuropa etc.)
- Übersicht zu den Stats
- Ansicht der News (z.B. für Events)
- "Next Button", um die nächste Runde zu starten
- Anzeige der (zu verbleibenden) Runden

## Events
- keine Randomisierung, aber starke Reduzierung der Events auf "Infektion einer neuen Region" (z.B. einmal in Runde 3)

## Maßnahmen
- Aufklärung
    - Maßnahme 1
    - Maßnahme 2
    - Maßnahme ...
- Einschränkung
    - ...
- Globale Super-Maßnahme
    - ...

## Ende des MvPs mit festen Win-Lose Texten
- Übertreffen von 70% Infizierten global --> Message: Nach X Wochen hat das Level der Infizierten 70% übertroffen; dabei sind X Personen ums Leben gekommen