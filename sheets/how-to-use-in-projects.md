# Wie könnte man Snippets in Projekte integrieren?

Grundsätzlich ist die Idee, dass jeder Snippets individuell für sich selber und seine Bedürfnisse anlegt. Um jedoch zu vermeiden, dass man für ein Projekt seine Autovervollständigung unnötig zumüllt und damit nicht jeder in einem Projekt die Projektspezifischen Snippets nicht immer wieder kopieren muss, können diese auch im Projekt Kontext angelegt werden. Dabei ist zu beachten, dass die Projekt-Snippets im `.vscode` Ordner abgelegt werden.

Damit nur die Snippets aus dem `.vscode` Ordner in Git hinzugefügt wird, sollte die `.gitignore` wie folgt angepasst werden:

```git
.vscode/*
!.vscode/*.code-snippets
```

Dadurch wird in Zukunft der `.vscode` Ordner nicht mehr von Git ignoriert. Allerdings jeglicher Inhalt bis auf die die `*.code-snippets` Snippets.
