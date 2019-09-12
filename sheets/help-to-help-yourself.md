# Hilfe zur selbst Hilfe (Gute Seiten für einen Überblick und zum Vertiefen)

Unter [drafts](./../drafts/) liegen ein paar hilfreiche Snippets, die beim Erstellen eigener Snippets hilfreich sind und können als Vorlagen verwendet werden können.

## Seiten
- [User defined snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets)  
  Offizielle VS Code Snippet Dokumentation
- [Snippet Generator](https://snippet-generator.app/?description=&tabtrigger=&snippet=&mode=vscode)  
  Generiert Snippets für VS Code, Atom und Sublime Text

## Tipps
Innerhalb von Quotes (einfache oder doppelte) funktioniert die Autovervollständigung der Snippets nicht. Dafür kann das Command `showSnippets` via Key Binding aufgerufen werden.  
```json
{ "key": "ctrl+alt+s", "command": "editor.action.showSnippets" }
```

Snippets können auch über Shortcuts aufgerufen werden.  
```json
{
  "key": "ctrl+k 1",
  "command": "editor.action.insertSnippet",
  "when": "editorTextFocus",
  "args": {
    "langId": "javascript",
    "name": "For_Loop"
  }
}
```
