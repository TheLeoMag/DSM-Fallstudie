# Titanic-Fallstudie

Wir untersuchen, welche Angaben mit dem Überleben auf der Titanic zusammenhängen, und erstellen Vorhersagen für 418 Personen. Die Erklärungen, Tabellen und Grafiken stehen direkt in den Notebooks.

Die gespeicherten Ergebnisse lassen sich auch ohne Ausführung der Zellen ansehen.

| Reihenfolge | Notebook | Inhalt |
|---|---|---|
| 0 | [Einzelne Angaben](00_Univariate_Deskriptive_Analyse.ipynb) | Werte, Verteilungen und fehlende Angaben |
| 1 | [Zusammenhänge](01_Exploration.ipynb) | Überleben nach Geschlecht, Alter und Ticketklasse |
| 2 | [Zusätzliche Merkmale](02_Feature_Engineering_und_Auswahl.ipynb) | Ideen zu Familie, Titeln, Tickets und Kabinen |
| 3 | [Modellvergleich](03_Modellvergleich.ipynb) | Drei verschiedene Ansätze vergleichen und auswählen |
| 4 | [Ausgewählte Modelle](04_Gewinner_Modell.ipynb) | Vorhersagen erklären, prüfen und speichern |

Die Ergänzungen [logistische Regression](04_Logistic_Regression.ipynb), [Entscheidungsbaum](04_Extended_Decision_Tree.ipynb) und [KNN](04_KNN.ipynb) erklären jeweils einen Ansatz genauer.

Zum erneuten Berechnen die Notebooks in dieser Reihenfolge öffnen und jeweils „Alle Zellen ausführen“ wählen. Der benötigte Projektcode steht vollständig in den Notebooks. Notebook 3 benötigt einige Minuten.

Für die Einrichtung mit Python 3.13 in PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

In VS Code die Erweiterungen „Python“ und „Jupyter“ verwenden und `.venv` als Notebook-Kernel auswählen.

`train.csv` enthält 891 Personen mit bekanntem Überleben; für die Personen in `test.csv` ist es unbekannt. Aufgabenstellung und Skriptum liegen als PDF im Projektordner. Originale Spaltennamen bleiben erhalten, damit die Zuordnung zu den Daten einfach ist.

Im Ordner `abbildungen` liegen die aktuellen Grafiken für die Präsentation. `ergebnisse` enthält benötigte Zwischenstände, wichtige Vergleiche und eine ausführliche Vorhersagetabelle mit Namen und Wahrscheinlichkeiten. Die übrigen Tabellen stehen direkt in den Notebooks.

`submission.csv` enthält die Vorhersagen des in Notebook 3 gewählten besten Modells. Die drei Dateien `submission_knn.csv`, `submission_logistic_regression.csv` und `submission_decision_tree.csv` enthalten die Vorhersagen der einzelnen Ansätze. Eine Überlebensquote ist der Anteil Überlebender; die Genauigkeit ist der Anteil richtiger Vorhersagen. Für die Testpersonen kann die Genauigkeit hier nicht berechnet werden.
