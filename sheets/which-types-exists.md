# Was für Arten gibt es?

In VS Code gibt es zwei Arten von Snippets.
1. Globale Snippets \<Allgemeiner Name\>`.code-snippets`
2. Sprach Snippets \<Sprach Id\>`.json`

## Globale Snippets
Globale Snippets sind oftmals nicht nur Code-Blöcke, sondern auch Konfigeinträge oder manchmal auch ganze Dateirümpfe. Damit man nicht die Übersicht vor lauter globalen Snippets verliert (wenn z. B. die aktuelle Programmiersprach nicht passt) haben die Globalen Snippets noch das zusätzliches Flag `scope`. Über das `scope`-Flag kann festgelegt werden, in welchen Kontexten ein Snippet angezeigt wird.  
(Beispiel: [config.code-snippets](./../drafts/config.code-snippets))

## Sprach Snippets
Sprach Snippets sind Snippets die nur für eine Spezielle Sprach gedacht sind. Sie besitzen **kein** `scope`-Flag, da dieses bereits als Dateiname angegeben wurde.  
(Beispiel: [javascript.json](./../examples/javascript.json))

```json
{
  "snippet_name": {
    "prefix": "trigger",
    "scope": "context (language id)",
    "body": [
      "Text which will be generated.",
      "Each line stand for a real line."
    ],
    "description": "For Loop"
  }
}
```
