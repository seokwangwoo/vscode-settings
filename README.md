# vscode-settings
My vscode settings and keybindings

## Settings
```json
{
   "workbench.colorTheme": "Visual Studio 2017 Dark - C++",
   "editor.bracketPairColorization.enabled": false,
   "editor.fontFamily": "'MyricaM M', Consolas, 'Courier New', monospace",
   "editor.fontSize": 15,
   "editor.wordSeparators": "`~!@#$%^&*()-=+[{]}\\|;:'\",.<>/?：",

   // extensions settings
   "theme-by-language.themes": {
      "python": "Visual Studio Dark - C++",
      "*": "Visual Studio 2017 Dark - C++"
   },
   "vim.easymotion": true,
   "vim.useSystemClipboard": true,
   "vim.insertModeKeyBindings": [
      {
         "before": ["j", "j"],
         "after": ["<Esc>"]
      }      
   ],
   "vim.normalModeKeyBindingsNonRecursive": [
      {
         "before": ["<C-p>"],
         "commands": ["workbench.action.quickOpen"],
         "silent": true
      },
      {
         "before": ["J"],
         "after": ["5", "J"],
      },
      {
         "before": ["K"],
         "after": ["5", "K"],
      },
      {
         "before": ["<Leader>", "j"],
         "after": ["J"]
      },
      {
         "before": ["<Leader>", "t", "t"],
         "after": [":tabnew"]
      },
      {
         "before": ["<Leader>", "t", "n"],
         "after": [":tabnext"]
      },
      {
         "before": ["<Leader>", "t", "n"],
         "after": [":tabprev"]
      },
      {
         "before": ["<Leader>", "t", "p"],
         "after": [":tabo"]
      },
      {
         "before": ["<Leader>", "/"],
         "after": [":noh"]
      },
      {
         "before": ["u"],
         "after": [],
         "commands": [
            {
               "command": "undo",
               "args": []
            }
         ],
         "silent": true,
      },
      {
         "before": ["<C-r>"],
         "after": [],
         "commands": [
            {
               "command": "redo",
               "args": []
            }
         ],
         "silent": true,
      },
      {
         "before": ["<C-h>"],
         "after": ["<C-w>", "h"],
      },
      {
         "before": ["<C-l>"],
         "after": ["<C-w>", "l"],
      },
   ],
   "vim.handleKeys": {
      "<C-b>": false,
      "<C-t>": false,
      "<C-w>": false
   },
   "vim.leader": "<space>",
   "vim.hlsearch": true,
   "vim.smartRelativeLine": true,
}

## Keybindings
```json
[
    {
        "key": "f5",
        "command": "workbench.action.debug.selectandstart",
        "when": "debugState != 'stopped'"
    },
    {
        "key": "ctrl+shift+b",
        "command": "-workbench.action.tasks.build",
        "when": "taskCommandsRegistered"
    },
    {
        "key": "ctrl+shift+b",
        "command": "workbench.action.tasks.runTask"
    },
    {
        "key": "ctrl+oem_minus",
        "command": "workbench.action.navigateBack",
        "when": "canNavigateBack"
    },
    {
        "key": "shift+alt+r",
        "command": "revealFileInOS"
    },
    {
        "key": "shift+alt+r",
        "command": "-revealFileInOS",
        "when": "!editorFocus"
    },
    {
        "key": "ctrl+shift+f",
        "command": "workbench.action.findInFiles",
        "when": "!filesExplorerFocus"
    },
    {
        "key": "ctrl+shift+f",
        "command": "-workbench.action.findInFiles"
    },
    {
        "key": "ctrl+oem_7",
        "command": "workbench.action.focusActiveEditorGroup",
        "when": "!editorTextFocus"
    },
    {
        "key": "ctrl+oem_3",
        "command": "workbench.action.terminal.toggleTerminal",
        "when": "editorTextFocus"
    },
    {
        "key": "ctrl+oem_3",
        "command": "-workbench.action.terminal.toggleTerminal",
        "when": "terminal.active"
    },
    {
        "key": "ctrl+shift+f",
        "command": "filesExplorer.findInFolder",
        "when": "explorerViewletVisible && filesExplorerFocus && !inputFocus"
    },
    {
        "key": "shift+alt+f",
        "command": "-filesExplorer.findInFolder",
        "when": "explorerResourceIsFolder && filesExplorerFocus && foldersViewVisible && !inputFocus"
    }
]
