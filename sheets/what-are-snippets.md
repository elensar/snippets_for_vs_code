# Was sind die Snippets und wie sehen diese aus?

Snippets sind in erste Linie einfache Textbausteine. Im Allgemeinen besitzen sie keine oder nur sehr wenig Logik und sind vorrangig dafür gedacht sich wiederholende Textblöcke schneller zu generieren. Das spart am Ende nicht nur Zeit, sondern macht auch den Code sicherer, da seltener Code vergessen wird und auch lesbarer, da der Text immer gleich formatiert ist. Ein weiterer Vorteil der Snippets ist, dass sie in der Regel Betriebssystem unabhängig sind und somit überall verwendet werden können.

Snippets können in VS Code in der Regel aus den folgenden drei Quellen stammen:
- von VS Code
- [eigene Snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets)
- über den [Extension Marketplace](https://code.visualstudio.com/docs/editor/extension-gallery)

In VS Code werden Snippets als `JSON` oder `JSONC` gespeichert. Je nach Editor wird ein anderes Format für die Snippets verwendet. Um dennoch nicht für jeden Editor alle Snippets händisch neu schreiben zu müssen, kann auch die Seite [Snippet Generator](https://snippet-generator.app/) verwendet werden.

Beispiel für eine for loop:
```json
{
  "For_Loop": {
    "prefix": "for",
    "scope": "javascript",
    "body": [
      "for (const ${2:element} of ${1:array}) {",
        "\t$0",
      "}"
    ],
    "description": "For Loop"
  }
}
```

Ergebnis:
```javascript
for (const element of array) {
  <code>
}
```

Im oberen Beispiel sind zwei Besonderheiten der Snippets zu sehen.
1. In Snippets können Platzhalter eingebaut werden, die über `$1` und `$2` angesprungen werden können. Eine Besonderheit ist hierbei, dass die Zahl nach `$` die Reihenfolge angibt. `$0` wird dabei **immer** als letztes angesprungen.
2. Außerdem können **default** texte hinter der Zahl angeben werden. Dieser wird angezeigt wird aber beim Anspringen so selektiert, das dieser gleich überschrieben werden kann.
