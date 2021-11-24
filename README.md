# Roll20 Macros - `rmacro`
[![VSMarket: rmacro](https://vsmarketplacebadge.apphb.com/version/anduh.rmacro.svg?color=blueviolet&logo=visual-studio-code&style=?style=for-the-badge)](https://marketplace.visualstudio.com/items?itemName=anduh.rmacro)
[![installs](https://img.shields.io/vscode-marketplace/d/anduh.rmacro?style=flat-square)](https://marketplace.visualstudio.com/items?itemName=anduh.rmacro)

[![Twitter: @anduh_ ](https://img.shields.io/badge/twitter-%40anduh%5F-blue)](https://twitter.com/anduh_)
[![Patreon Donate](https://img.shields.io/badge/donate-patreon-orange)](https://www.patreon.com/anduh)


Support & Syntax Highlight for [Roll20](https://roll20.net/)'s [macro language](https://wiki.roll20.net/Macro_Guide).


## Features


**Bracket pairing**

- roll20 macros (`@{ }`, `?{ }`, `%{ }`, `&{ }`)
- correctly distinguished `[[ ]]`/`{{ }}` from `[ [ ] ]`/`{ { } }`
- identifies 1st and 2nd order query nesting & HTML replacement characters

<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/bracket-recognition.gif">

**Syntax & keyword highlights**

- inline roll labels
- roll, macro & API commands (e.g. `/r`, `!example` `#dex`)
- normal and fate (`dF`) die
- some keywords (`selected`, `target`, `%%NEWLINE%%`, `max`, `cf`, `ceil`, `tracker`)
- special characters used in macros (e.g. `~,|#=+`, and html replacment characters) 

<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/ex1.gif">


### Example
Macro nesting bracket highlight

<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/replacement-recognition-bracket.png">


Missing bracket stands out
<img src="https://raw.githubusercontent.com/Anduh/rmacro/main/images/rmacro-typo.gif">

### Use
VScode shows/recognizes "rmacro"-syntax highlight when a file is saved with `.roll` or `.rmacro` suffix.



## Other

The extension sets `editor.bracketPairColorization.enabled`: `true` for rmacro files. If this is overruled by user settings, *all* bracket highlights will disappear, not just the extra coloring.