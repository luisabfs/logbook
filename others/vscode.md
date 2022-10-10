## [ERROR] Shell integration failed to activate
Disable shell integration automatic injection with this line on `settings.json`:

```JSON
"terminal.integrated.shellIntegration.enabled": false,
```

And then install it manually in your `.zshrc`:

```
[[ "$TERM_PROGRAM" == "vscode" ]] && . "$(code --locate-shell-integration-path zsh)"
```

[Link](https://github.com/microsoft/vscode/issues/157611#issuecomment-1209528676)
