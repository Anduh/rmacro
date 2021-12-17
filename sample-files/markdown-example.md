# Roll20 examples

sheet code
```html
<input type="number" name="attr_str" value="3">
<button type="roll" name="roll_str" value="/r d20+@{str}">STR</button>
```
roll20 macro

```rmacro
/em has a carry capasity of [[@{str}*10]], having a Strength of **@{str}**.
```

```roll20
/em has a carry capasity of [[@{str}*10]], having a Strength of **@{str}**.
```

```r20
/em has a carry capasity of [[@{str}*10]], having a Strength of **@{str}**.
```

,
    {
      "begin": "(\\${)",
      "end": "(})",
      "beginCaptures": {
        "1": {
          "name": "entity.name.tag"
        }
      },
      "endCaptures": {
        "1": {
          "name": "entity.name.tag"
        }
      },
      "patterns": [
        {
          "include": "source.ts#template-substitution-element"
        },
        {
          "include": "source.js"
        }
      ]
    }