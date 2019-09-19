# What are the snippets and what do they look like?

Snippets are first and foremost simple text modules. In general, they have no or very little logic and are primarily intended to generate repeating text blocks faster. This not only saves time in the end, but also makes the code more secure, since code is rarely forgotten and also more readable, since the text is always formatted the same. Another advantage of the snippets is that they are usually operating system independent and can be used everywhere.

Snippets in VS Code can usually come from the following three sources:
  - from VS Code itself
  - [own snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets)
  - via the [Extension Marketplace](https://code.visualstudio.com/docs/editor/extension-gallery)

In VS Code, snippets are stored as `JSON` or `JSONC`. Depending on the editor, a different format is used for the snippets. To avoid having to manually rewrite all snippets for each editor, you can also use the [Snippet Generator](https://snippet-generator.app/) page.

Example of a for loop:
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

Outcome:
```javascript
for (const element of array) {
  <code>
}
```

The example above shows two special features of the snippets.
  1. In snippets placeholders can be inserted, which can be jumped to via `$1` and `$2`. A special feature is that the number after `$` indicates the order. `$0` is the last number to jump to **always**.
  2. you can also specify **default** texts after the number. This will be displayed but will be selected during the jump so that it can be overwritten immediately.
