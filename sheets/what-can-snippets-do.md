# Was kann man alles mit Snippets machen?

Es gibt vier Variante der Tabstops:
1. (normale) [Tabstops](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_tabstops)  
  `$1`, `$2`, `$0`
2. [Placeholders](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_placeholders)  
  `${1:foo}`
3. [Choice](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_choice)  
  `${1|one,two,three|}`
4. [Variables](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_variables)  
  `$name` oder `${name:default}`

Es ist möglich die verschiedenen Arten der Tabstops zu kombinieren. Damit können z. B. kleinere Abhängigkeiten abgebildet werden.
Beispiel:  
`${1:Foo ${2:Bar}} $3`  
Placholder `$2` wird nicht angesprungen, wenn der Placholder `$1` gelöscht wird. Tabstop `$3` würde jedoch trotzdem korrekt angesprungen werden.

Weiterhin ist es möglich Placeholders auch über mehrer Zeilen zu setzen. Das kann vor allem bei Datei Templates hilfreich sein.
Beispiel:  
[examples.code-snippets](./../examplex/examples.code-snippets) --> `placeholder_beispiel`

Wenn mehrere eigene Variablen angegeben sind, werden diese der Reihe nach angesprungen.  
Es gibt außerdem eine Reihe von Variablen die gewisse Informationen bereitstellen. Eine Liste dieser Variablen ist unter [General Snippets](./../drafts/GeneralSnippets.code-snippets) oder auf der [Offiziellen Seite](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_variables) zu finden.

**Hinweis**: Platzhalter innerhalb eines Choice sind aktuell nicht möglich.
