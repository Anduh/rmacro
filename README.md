# Roll20 Macros - `rmacro`
[![VSMarket: rmacro](https://vsmarketplacebadge.apphb.com/version/anduh.rmacro.svg?color=blueviolet&logo=visual-studio-code&style=?style=for-the-badge)](https://marketplace.visualstudio.com/items?itemName=anduh.rmacro)
[![installs](https://img.shields.io/vscode-marketplace/d/anduh.rmacro?style=flat-square)](https://marketplace.visualstudio.com/items?itemName=anduh.rmacro)
![Last Commit](https://img.shields.io/github/last-commit/Anduh/rmacro)
![Contributions](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)

[![Twitter: @anduh_ ](https://img.shields.io/badge/twitter-%40anduh%5F-blue)](https://twitter.com/anduh_)
[![Patreon Donate](https://img.shields.io/badge/donate-patreon-orange)](https://www.patreon.com/anduh)


Support & Syntax Highlight for [Roll20](https://roll20.net/)'s [macro language](https://wiki.roll20.net/Macro_Guide).

- [Roll20 Macros - `rmacro`](#roll20-macros---rmacro)
  - [Features](#features)
    - [Bracket pairing](#bracket-pairing)
    - [Syntax highlights](#syntax-highlights)
    - [Snippets](#snippets)
  - [Example](#example)
  - [Use](#use)
    - [Issues](#issues)
  - [Settings](#settings)
  - [Contribute](#contribute)
- [Related Extensions](#related-extensions)


## Features

### Bracket pairing
Automatic bracket pairing for roll20 syntax
- roll20 macros (`@{ }`, `?{ }`, `%{ }`, `&{ }`, `$[[ ]]`)
- correctly distinguished `[[ ]]`/`{{ }}` from `[ [ ] ]`/`{ { } }`
- identifies 1st and 2nd order query nesting & [HTML replacement characters](https://wiki.roll20.net/HTML_Entities)

<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/bracket-recognition.gif">

### Syntax highlights

- inline roll labels
- roll, macro & API commands (e.g. `/r`, `!example` `#dex`)
- normal and fate (`dF`) die
- some keywords (`selected`, `target`, `%%NEWLINE%%`, `max`, `cf`, `ceil`, `tracker`)
- special characters used in macros (e.g. `~,|#=+`, and [HTML Entities]([HTML replacement characters](https://wiki.roll20.net/HTML_Entities)) 
- **rmacro highlight in other languages**: 
  - js/pug (everything inside ``roll` ` `` will highlight)
  - markdown (fenced codeblocks, with `rmacro` set as language)

<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/ex1.gif">

### Snippets

- as you type, some matching suggestions will be provided
- also includes couple of more advanced examples

<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/snippets.gif">

## Example
Macro nesting bracket highlight

<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/replacement-recognition-bracket.png">


Missing bracket stands out
<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/rmacro-typo.gif">

Rmacro syntax highlight in javascript:
<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/rmacro-in-js.png">

Rmacro syntax highlight in markdown files:

<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/markdown-codeblock.png">


## Use
VScode shows/recognizes "rmacro"-syntax highlight when:

- a file has the filetype `.roll` (`.rmacro`/`.roll20`/`.r20macro` also works)
- inside [fenced codeblocks](https://www.markdownguide.org/extended-syntax/#fenced-code-blocks) of markdown files, with `rmacro` set as the language.
- inside `.js` and `.pug`-files, when the macro is inside a [tagged template literal](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals#tagged_templates) with `rmacro` as the tag 

The autocompletions work only in `.roll`/`.rmacro`/`.roll20`/`.r20macro`-files

This extension also works on [vscode.dev](https://vscode.dev)

You can download the [sample files](https://github.com/Anduh/rmacro/tree/v111/sample-files)) to get started.

<a href="https://github.com/Anduh/rmacro/tree/v111/sample-files/example.roll" target="_blank">Download `example.roll`</a>

### Issues

Sometimes extra spaces are needed to keep the bracket highlight working correctly.

When nesting double- & single-bracket syntax, leave a `space` after the last inner character.

Good:
```rmacro
{{name=@{character_name} }}
```
Bad:
```rmacro
{{name=@{character_name}}}
```

## Settings

Sets following default setting for `.rmacro`-files:

* `"editor.bracketPairColorization.enabled": true` - If this is overruled by user settings, *all* bracket highlights will disappear, not just the extra coloring.
* `"editor.wordWrap": "on"` - wraps lines by default. roll20 macros are often on a single line, and this improves readability.

Installs an extended version of [file-icons](https://marketplace.visualstudio.com/items?itemName=file-icons.file-icons) Theme, which changes the the fileicon for `.rmacro`-files & some roll20 Sheet/API development-related filenames.

## Contribute
repo: [Anduh/rmacro](https://github.com/Anduh/rmacro)

You can help even without knowing how VS Code extensions work. Here are a few concrete parts to start from: 

* More [rmacro Snippets](https://github.com/Anduh/rmacro/tree/main/snippets): if you look at the existing snippets for `rmacro`, you can follow the same patterns and expand the collection of snippets easily.
  * About:[VS Code Snippet Syntax](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_snippet-syntax)
* improve [rmacro syntax highlight](https://github.com/Anduh/rmacro/blob/main/syntaxes/rmacro.tmLanguage.json): 
  * [Regex](https://macromates.com/manual/en/regular_expressions) is used for recognizing things, and creating more of them, [Regexr.com](https://regexr.com/) is a good source.
    * example: 
  * [TextMate grammar](https://code.visualstudio.com/api/language-extensions/syntax-highlight-guide) is used for defining
  * About:[VSCode  Syntax Highlight](https://code.visualstudio.com/api/language-extensions/syntax-highlight-guide)


# Related Extensions

[Roll20 Sheet Dev](https://marketplace.visualstudio.com/items?itemName=anduh.roll20sheetdev) helps with [Character Sheet Development](https://wiki.roll20.net/Building_Character_Sheets).



