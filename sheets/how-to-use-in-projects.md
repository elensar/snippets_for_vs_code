# How could snippets be integrated into projects?

Basically, the idea is that each snippet is designed individually for itself and its needs. However, in order to avoid that you unnecessarily fill in your autocompletion for a project and that not everyone in a project has to copy the project-specific snippets again and again, they can also be created in the project context. Please note that the project snippets are stored in the `.vscode` folder.

So that only the snippets from the `.vscode` folder are added to Git, the `.gitignore` should be modified as follows:

```git
.vscode/*
!.vscode/*.code-snippets
```

This will prevent Git from ignoring the `.vscode' folder in the future. But any content except the `*.code-snippets` snippets.
