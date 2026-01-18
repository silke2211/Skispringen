Skispringen (ss619, em089, rd043, fl067, mr241)
---

1) Themenfeld:

Das Themenfeld umfasst die Karrierewege und Beziehungsstrukturen im professionellen Skispringen. Untersucht werden Athleten, Trainer, Vereine und Nationalteams sowie deren Verbindungen über einen Zeitraum von 25 Jahren. Grundlage sind öffentlich zugängliche FIS‑Daten zu Teilnahmen, Platzierungen, Nationalitäten und Rollenwechseln im internationalen Skispringen.


2) Literaturübersicht: Forschungsstand / vergleichbare Studien

- https://www.researchgate.net/profile/Luisa-Barthauer/publication/318236461_Karrierenetzwerke_und_ihr_Einfluss_auf_die_Laufbahnentwicklung/links/5a21148aa6fdcccd30e065c5/Karrierenetzwerke-und-ihr-Einfluss-auf-die-Laufbahnentwicklung.pdf (Lektüre zu Karrierenetzwerken und deren Einfluss auf die Laufbahnentwicklung)
- https://www.ssoar.info/ssoar/bitstream/handle/document/16503/ssoar-2004-2-horak_et_al-sportsystem_und_ausbildungskarrieren_von_spitzensportlerinnen.pdf?sequence=1&isAllowed=y&lnkname=ssoar-2004-2-horak_et_al-sportsystem_und_ausbildungskarrieren_von_spitzensportlerinnen.pdf (Laufbahnentscheidungen von österreichischen Spitzensportlern in verschiedenen Sportarten, darunter “Skisprunglauf” - das sollte ja Skispringen sein, I guess)
- https://link.springer.com/book/10.1007/978-3-658-33588-5 1. Wodurch zeichnen sich hauptberufliche Personalstrukturen und Karrieren von Führungskräften im organisierten Sport aus? 2. Wird bei den hauptberuflichen Personalstrukturen und Karrieren von Führungskräften im organisierten Sport Geschlecht zu einer bedeutsamen Ordnungskategorie? Wie lassen sich Prozesse und Strukturen der Relevanzwerdung von Geschlecht beschreiben und erklären? → Not sure ob uns das irgendwie hilft oder nicht
- https://www.researchgate.net/profile/Otto-Penz/publication/240609976_Soziale_Bedingungen_des_Spitzensports/links/54b90e1b0cf28faced626920/Soziale-Bedingungen-des-Spitzensports.pdf (Lektüre über Laufbahnentscheidungen und Karriereplanungen und deren Abhängigkeit von strukturellen Voraussetzungen (also ob die Athlet(inn)en einer populären Sportart oder einer so genannten Randsportart angehören bzw. inwiefern Sportschulen für einzelne Sportarten existieren), geht auf um Skispringen)
- https://www.tandfonline.com/doi/full/10.1080/16138171.2019.1693143 Wie sind Netzwerke innerhalb von jungen Sportteams. Skifahren und Biathlon sind unter anderem aufgeführt.


3) Fragestellung/Arbeitshypothese:

Fragestellung:
Uns interessiert, wie Athleten und Trainer im internationalen Skispringen über Vereine und Nationalteams miteinander verknüpft sind und welche Karrierepfade besonders häufig vorkommen. Zudem möchten wir herausfinden, welche Vereine besonders viele erfolgreiche Athleten hervorbringen, wie Trainerkarrieren zwischen Nationen verlaufen und welche Länder über Athleten‑ und Trainerbewegungen eng miteinander verbunden sind.

Arbeitshypothese: 
Traditionelle Skisprungnationen (z. B. Österreich, Norwegen, Deutschland) weisen eine hohe Zentralität auf, da sie sowohl viele erfolgreiche Athleten hervorbringen als auch international gefragte Trainer beschäftigen. Trainerwechsel und Athletenkarrieren verstärken die Verbindungen zwischen Nationen zusätzlich.


4) Datenzugang klären, Codebuch entwickeln

Die Daten stammen aus der öffentlich zugänglichen FIS‑Datenbank. Dort finden sich Informationen zu Athleten, Trainern, Nationalitäten, Vereinen, Platzierungen und Teilnahmen an internationalen Wettbewerben.
Erfasst werden die letzten 25 Jahre aus zwei zentralen Eventtypen:

- Olympische Winterspiele
- Vierschanzentournee

Die Erhebung erfolgt durch systematische Extraktion der Podestlisten, Trainerangaben und Vereinszugehörigkeiten. Der Aufwand ist moderat, da die Daten strukturiert vorliegen.

Link zum Codebuch: https://github.com/silke2211/Skispringen/blob/main/Codebuch_Skispringen.csv?plain=1

5) Beispieldaten (Edge- und Nodelist auf github)

Link zur Edgelist: https://github.com/silke2211/Skispringen/blob/main/Edgelist_Skispringen.csv

Link zur Nodelist: https://github.com/silke2211/Skispringen/blob/main/Nodelist_Skispringen.csv

6) Mögliche Probleme und Herausforderungen

→ Schwierigkeit: Multimodales Netzwerk mit Athleten, Trainern, Vereinen und Nationen erschwert den direkten Vergleich von Netzwerkmetriken.
Lösung: Zentralitätsmaße getrennt nach Knotentypen / in spezifischen Teilnetzwerken interpretieren..

→ Sind die Informationen für die Trainer alle öffentlich? Reicht die FIS-Datenbank dafür? 
Lösung: Info bedarf möglicherweise erweiterte Recherche, vielleicht auf Vereinswebsiten?

→ Wie dokumentieren wie Trainer- und Athletenwechsel über die Jahre in einem Netzwerk?
Lösung: Kantenattribut year für die Zugehörigkeiten zu den Vereinen?

→ Gibt es Athleten, die später zu Trainern werden? → könnte zu einer verwirrenden Darstellung im Netzwerk führen
Lösung: Möglicherweise zwei Knoten für eine Person (Athlet: XY_A; Trainer: XY_T)

→ Wir haben viele Akteure, was in der Visualisierung schnell unübersichtlich aussehen kann. Man könnte wichtige Verbindungen vergessen


