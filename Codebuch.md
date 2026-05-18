# Codebuch: Skispringen

## 1. Edgelist 


| Variable | Beschreibung |
| :--- | :--- |
| **from** | Definiert den Sender in gerichteten Netzwerken. Entspricht der `id` in der Nodelist. Keine Sonderzeichen, nur ein Wort. |
| **to** | Definiert den Empfänger. Entspricht der `id` in der Nodelist. Keine Sonderzeichen, etc. |
| **relation** | Art der Beziehung, definiert nach folgendem Schlüssel: |
| | 1 = Athlet → Verein |
| | 2 = Athlet → Nation |
| | 3 = Trainer → Nation |
| | 4 = Trainer → Athlet |
| | 5 = Verein → Nation |
| | 6 = Trainer → Verein |
| | 7 = Athlet → Event |
| | 8 = Trainer → Event |
| | 9 = Verein → Region |
| | 10 = Region → Land |
| **weight** | Ausprägung des Erfolgs: <br> 1 = kein Podium <br> 2 = 3. Platz <br> 3 = 2. Platz <br> 4 = 1. Platz |
| **event** | Art des Wettbewerbs: <br> `wc` = World Championship (Normalschanze) <br> `oly` = Olympische Winterspiele (Normalschanze) |
| **year** | Jahr der Teilnahme am Wettbewerb. |

---

## 2. Nodelist 


| Variable | Beschreibung |
| :--- | :--- |
| **id** | Eindeutige Identifikation jedes einzelnen Knotens.<br> Die id setzt sich aus dem Anfangsbuchstaben des Vornamen und des Anfangsbuchstaben des Nachnamen der Springer/Trainer zusammen. Wenn sich ids gedoppelt haben, wurden die letzten beiden Ziffern des Geburtsjahres ergänzt. <br> Vereine wurden jeweils durch v_vereinsname gekennzeichnet.<br> Regionen wurden mit r_regionsname gekennzeichnet. <br> Nationen wurden mit dem ISO Code gekennzeichnet.<br> Die Events haben das Kürzel oly und wc erhalten, zusammen mit den letzten beiden Ziffern des Veranstaltungsjahres.   |
| **name** | Name oder Bezeichnung des Knotens. |
| **type** | Unterscheidung der Akteure/Organisationen: <br> 1 = Athlet <br> 2 = Trainer <br> 3 = Verein <br> 4 = Nation <br> 5 = Event <br> 6 = Region |
| **country** | Für welches Land tritt der Athlet/Trainer an. |
| **nationality** | Staatsangehörigkeit. |
| **team** | Aus welchem Verein kommt der Athlet/Trainer. |
| **debut_year** | Jahr, in welchem der Athlet/Trainer angefangen hat. |
| **last_year** | Jahr, in welchem der Athlet/Trainer aufgehört hat. |
| **active** | Zeigt an, ob der Athlet/Trainer aktuell noch aktiv ist. |
| **year_birth** | Geburtsjahr des Athleten/Trainers. |

---

## 3. Allgemeine Hinweise

### Fehlende Werte (NA)
* Fehlende Werte werden als `NA` definiert.

### Nicht berücksichtigte Fälle / Sonderregeln
* **Karriereverlauf:** Pausen von Athleten werden nicht berücksichtigt. Dokumentiert werden nur der Beginn (`debut_year`) und das Ende (`last_year`) der Karriere.
* **Disqualifikationen:** Werden nicht berücksichtigt (egal ob im Vorhinein oder im Nachhinein wegen Doping etc.).
* **Qualifikation:** Nichtqualifikationen für Olympia werden nicht erfasst.
* **Teilnahme:** Anmeldungen ohne tatsächliche Teilnahme am Wettkampf werden nicht berücksichtigt.
