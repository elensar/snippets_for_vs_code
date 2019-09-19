# What types are there?

There are two types of snippets in VS Code.
1. Global Snippets \<Allgemeiner Name\>`.code-snippets`
2. Language Snippets \<Sprach Id\>`.json`

## Global Snippets
Global snippets are often not only code blocks, but also config entries or sometimes whole file trunks. So that you don't lose track of all the global snippets (e.g. if the current programming language doesn't fit), the global snippets have the additional flag `scope`. The `scope` flag can be used to specify the contexts in which a snippet is displayed.  
(Example: [config.code-snippets](./../drafts/config.code-snippets)))

## Language Snippets
Language snippets are snippets that are only intended for one specific language. They have **no** `scope` flag, because this was already specified as file name.  
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
