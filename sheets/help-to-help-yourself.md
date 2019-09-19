# Help to help yourself (good pages for an overview and to deepen)

Under [drafts](./../drafts/) there are a few helpful snippets which are helpful when creating your own snippets and can be used as templates.

## Sides
  - [User defined snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets)  
    Official VS Code Snippet Documentation
  - [Snippet Generator](https://snippet-generator.app/?description=&tabtrigger=&snippet=&mode=vscode)  
    Generates snippets for VS Code, Atom and Sublime Text

## Tips
Within quotes (single or double) the auto-completion of snippets does not work. Therefore the command `showSnippets` can be called via Key Binding.  
```json
{ "key": "ctrl+alt+s", "command": "editor.action.showSnippets" }
```

Snippets can also be called via shortcuts.  
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
