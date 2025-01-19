# switch between windows (on win)

```json
{
    "key": "ctrl+tab",
    "command": "workbench.action.quickOpenRecent",
    "when": "!inRecentFilesPicker"
},
{
    "key": "ctrl+tab",
    "command": "workbench.action.quickOpenNavigateNextInRecentFilesPicker",
    "when": "inQuickOpen && inRecentFilesPicker"
},
{
    "key": "shift+ctrl+tab",
    "command": "workbench.action.quickOpenNavigatePreviousInRecentFilesPicker",
    "when": "inQuickOpen && inRecentFilesPicker"
}
```

and also add to user settings

```json
"terminal.integrated.commandsToSkipShell": [
    ...,
    "workbench.action.quickOpenRecent",
    "workbench.action.quickOpenNavigateNextInRecentFilesPicker",
    "workbench.action.quickOpenNavigatePreviousInRecentFilesPicker"
]
```
