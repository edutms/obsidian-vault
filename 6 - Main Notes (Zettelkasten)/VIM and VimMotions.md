2025-07-17 14:29

### Status: #baby

### Tags: [[software-engineering]]

# VimMotions

What is it?
A fancy and pedantic way of coding where I should not touch my mouse and or my arrow keys. It goes well alongside my mechanical keyboard that was lost in my wardrobe.

To setup Vim is not trivial, so you have to add tons of new keybindings on vscode settings file. 


Here are them:
```
"vim.leader": "<Space>",

"vim.hlsearch": true,

"vim.insertModeKeyBindings": [

{

"before": ["j", "j"],

"after": ["<Esc>"]

}

],

"vim.handleKeys": {

"<tab>": false,

"<C-i>": false

},

"vim.normalModeKeyBindingsNonRecursive": [

// NAVIGATION

// switch b/w bufferasda

{ "before": ["<S-h>"], "commands": [":bprevious"] },

{ "before": ["<S-l>"], "commands": [":bnext"] },

  

// splits

{ "before": ["leader", "v"], "commands": [":vsplit"] },

{ "before": ["leader", "s"], "commands": [":split"] },

  

// panes

{

"before": ["leader", "h"],

"commands": ["workbench.action.focusLeftGroup"]

},

{

"before": ["leader", "j"],

"commands": ["workbench.action.focusBelowGroup"]

},

{

"before": ["leader", "k"],

"commands": ["workbench.action.focusAboveGroup"]

},

{

"before": ["leader", "l"],

"commands": ["workbench.action.focusRightGroup"]

},

// NICE TO HAVE

{ "before": ["leader", "w"], "commands": [":w!"] },

{ "before": ["leader", "q"], "commands": [":q!"] },

{ "before": ["leader", "x"], "commands": [":x!"] },

{

"before": ["[", "d"],

"commands": ["editor.action.marker.prev"]

},

{

"before": ["]", "d"],

"commands": ["editor.action.marker.next"]

},

{

"before": ["<leader>", "c", "a"],

"commands": ["editor.action.quickFix"]

},

{ "before": ["leader", "f"], "commands": ["workbench.action.quickOpen"] },

{ "before": ["leader", "p"], "commands": ["editor.action.formatDocument"] },

{

"before": ["g", "h"],

"commands": ["editor.action.showDefinitionPreviewHover"]

}

],

"vim.visualModeKeyBindings": [

// Stay in visual mode while indenting

{ "before": ["<"], "commands": ["editor.action.outdentLines"] },

{ "before": [">"], "commands": ["editor.action.indentLines"] },

// Move selected lines while staying in visual mode

{ "before": ["J"], "commands": ["editor.action.moveLinesDownAction"] },

{ "before": ["K"], "commands": ["editor.action.moveLinesUpAction"] },

// toggle comment selection

{ "before": ["leader", "c"], "commands": ["editor.action.commentLine"] }

],

"[typescriptreact]": {

"editor.defaultFormatter": "esbenp.prettier-vscode"

},

"go.toolsManagement.autoUpdate": true,

"[typescript]": {

"editor.defaultFormatter": "esbenp.prettier-vscode"

},

"[jsonc]": {

"editor.defaultFormatter": "esbenp.prettier-vscode"

}

}



```



## But why??
To look cool is the goal here. I want to become a ML/AI engineer, and looking dapper when coding is the way to go.

But really, it is to improve my coding skills. I sense that I'm spending a lot of time going  back and forth mouse, copying and pasting code snippets between files, so I hope this might help me in the journey ahead.


# References

https://www.youtube.com/watch?v=GST8we5uABo







