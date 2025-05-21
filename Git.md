| **Befehl**                    | **Beschreibung**                                                                                                             |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `git init`                    | Erstellt ein neues Git-Repository                                                                                            |
| `git clone <url>`             | Klont ein Remote-Repository lokal                                                                                            |
| `git status`                  | Zeigt den aktuellen Status der Dateien                                                                                       |
| `git add <datei>`             | Fügt Dateien zur Staging-Area hinzu                                                                                          |
| `git add .`                   | Fügt alle Änderungen im aktuellen Verzeichnis hinzu                                                                          |
| `git commit -m "Nachricht"`   | Speichert Änderungen mit Kommentar                                                                                           |
| `git push`                    | Schiebt lokale Commits zum Remote-Repository                                                                                 |
| `git pull`                    | Holt Änderungen vom Remote und merged sie                                                                                    |
| `git branch`                  | Zeigt lokale Branches an                                                                                                     |
| `git branch <name>`           | Erstellt einen neuen Branch                                                                                                  |
| `git checkout <branch>`       | Wechselt zu einem anderen Branch                                                                                             |
| `git checkout -b <branch>`    | Erstellt einen neuen Branch und wechselt zu ihm                                                                              |
| `git merge <branch>`          | Fügt den angegebenen Branch in den aktuellen Branch ein                                                                      |
| `git log`                     | Zeigt die Commit-Historie an                                                                                                 |
| `git diff`                    | Zeigt Änderungen zwischen Arbeitsverzeichnis und Staging                                                                     |
| `git remote -v`               | Zeigt die verbundenen Remote-Repositories                                                                                    |
| `git rebase <branch>`         | Nimmt deine aktuellen Commits und „spielt“ sie auf `<branch>` oben drauf — praktisch, um eine sauberere Historie zu erzeugen |
| `git rebase --continue`       | Nach einem Konflikt beim Rebase: Konflikte lösen und fortsetzen                                                              |
| `git rebase --abort`          | Rebase abbrechen und zum ursprünglichen Zustand zurückkehren                                                                 |
| `git rebase -i HEAD~<Anzahl>` | Interaktives Rebase der letzten `<Anzahl>` Commits starten, um z.B. zu squashen                                              |
| `git reset`                   | Entfernt **alle** Dateien aus der Staging-Area (unstagen)                                                                    |
| `git reset <datei>`           | Entfernt eine einzelne Datei aus der Staging-Area                                                                            |
| `git reset --hard`            | Setzt Arbeitsverzeichnis und Staging-Area auf letzten Commit zurück (Achtung: alle ungesicherten Änderungen gehen verloren!) |
| `git checkout -- <datei>`     | Setzt eine einzelne Datei im Arbeitsverzeichnis zurück (Änderungen gehen verloren)                                           |
