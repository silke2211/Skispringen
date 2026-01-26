# Codebuch: Skispringen

Dieses Dokument beschreibt die Struktur und die Variablen für die Erfassung des Netzwerks.

---
## 1. Nodelist
Die Nodelist beschreibt die Eigenschaften der einzelnen Knoten (Akteure/Organisationen).

| Variable | Beschreibung |
| :--- | :--- |
| **id** | Eindeutige Identifikation jedes einzelnen Knotens (Vertex). |
| **name** | Name oder Bezeichnung des Knotens. |
| **type** | Typ des Akteurs: <br> `1` = Athlet, `2` = Trainer, `3` = Verein, `4` = Nation, `5` = Event |
| **country** | Staatsangehörigkeit bzw. Land, für das gestartet wird (z.B. `NOR` für Norwegen). |
| **team** | Verein des Athleten oder Trainers. |
| **debut_year** | Jahr des Karrierestarts. |
| **last_year** | Jahr des Karriereendes. |
| **active** | Gibt an, ob der Athlet/Trainer aktuell noch aktiv ist. |
| **year_birth** | Geburtsjahr. |
| **NA** | Fehlende Werte: Feld leer lassen. R erkennt diese automatisch als *missing values*. |

---

## 2. Edgelist
Die Edgelist definiert die Beziehungen (Kanten) zwischen den einzelnen Akteuren.

| Variable | Beschreibung |
| :--- | :--- |
| **from** | Sender in gerichteten Netzwerken. Entspricht der **ID** in der Nodelist. (Keine Sonderzeichen, ein Wort). |
| **to** | Empfänger in Netzwerken. Entspricht der **ID** in der Nodelist. |
| **relation** | Art der Beziehung (Kantenstärke) basierend auf folgenden Skalen: |
| | `1` = Athlet → Verein |
| | `2` = Athlet → Nation |
| | `3` = Trainer → Nation |
| | `4` = Trainer → Athlet |
| | `5` = Verein → Nation (über Athleten verbunden) |
| | `6` = Trainer → Verein (falls frühere Karriere relevant) |
| | `7` = Athlet → Event |
| | `8` = Trainer → Event |
| **weight** | Anzahl/Art der Erfolge: <br> `1` = 1. Platz, `2` = 2. Platz, `3` = 3. Platz, `4` = kein Podium |
| **event** | Art des Wettbewerbs: <br> `vst` = Vierschanzentournee, `oly` = Olympische Winterspiele |
| **year** | Jahr der Teilnahme am Wettbewerb. |

---

## Wichtige Hinweise
* **Pausen:** Zeitweilige Unterbrechungen von Athleten bei Wettbewerben werden nicht berücksichtigt (nur Beginn und Ende der Karriere).
* **Nicht berücksichtigt:**
    * Disqualifikationen
    * Nichtqualifikationen für Olympische Spiele
