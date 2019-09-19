# What can you do with snippets?

There are four types of tab stops:
1. (normal) [Tabstops](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_tabstops)  
  `$1`, `$2`, `$0`
2. [Placeholders](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_placeholders)  
  `${1:foo}`
3. [Choice](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_choice)  
  `${1|one,two,three|}`
4. [Variables](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_variables)  
  `$name` oder `${name:default}`

It is possible to combine the different types of tabs. This allows you to map smaller dependencies, for example.
Example:  
`${1:Foo ${2:Bar}} $3`  
Placholder `$2` is not started if the Placholder `$1` is deleted. Tabstop `$3` would still be started correctly.

It is also possible to set placeholders over several lines. This can be especially useful for file templates.
Example:  
[examples.code-snippets](./../examplex/examples.code-snippets) --> `placeholder_example`

If several own variables are specified, they are jumped to one after the other.  
There are also a number of variables that provide certain information. A list of these variables can be found under [General Snippets](./../drafts/GeneralSnippets.code-snippets) or on the [Official Site](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_variables).

**Note**: Placeholders within a choice are currently not possible.
