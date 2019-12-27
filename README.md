# Interaction Markdown

---
⚠️ *This is just an idea for now, it does not really exist!*

---

> Interaction Markdown is a superset of [Markdown](https://commonmark.org/), that allow for quick, syntax-sugared prototyping.

The file extension is `.ixmd`.

While you *can* do everything described here with [Markdown's vanilla inline HTML feature](https://daringfireball.net/projects/markdown/syntax#html), Interaction Markdown offers writing syntaxes inline that support significant whitespace, like [Pug](https://github.com/pugjs/pug/blob/master/README.md#pug) and [Sass](https://sass-lang.com/documentation)

It also comes with the simplest of languages, [UI Lang](http://uilang.com/), to make things actually interactive.

## a) Interaction Markdown eats [Pug](https://github.com/pugjs/pug/blob/master/README.md#pug)

> [Pug](https://github.com/pugjs/pug/blob/master/README.md#pug) is a high-performance template engine heavily influenced by [Haml](http://haml.info/) and implemented with JavaScript for Node.js and browsers.

A small subset of pug can be written directly inline into `.ixmd` files

For example...

`.cat` -> `<div class=“cat”>`

`span.bff#dog` -> `<span class="bff" id=“dog”>`

You can also start a full block of pug with the keyword `pug`:

```
# A markdown headline

A markdown paragraph

- a bullet
- list with
- some items

pug
  .info This block is rendered completely as pug
  .info
    | Everything goes
    span.highlight#counter(data-counter="0") Because it is rendered as pure pug

```

## b) Interaction Markdown eats  indented Sass (and SCSS)  in style tags

> [Sass](https://sass-lang.com/) is the most mature, stable, and powerful professional grade CSS extension language in the world.

This also works:

```
<style lang="scss"></style>
  $dogcolor: brown;
  .dog {
    color: $dogcolor;
  }
</style>
```

Additionally, Interaction Markdown recognizes "`style`" as a keyword, to allow for a consistent significant whitespace experience.

```
style(lang=sass)
  $dogcolor: brown
  .dog
    color: $dogcolor
```


The standard feature of Markdown to write pure CSS in inline HTML style tags is still an option:

```
<style>
  :root {
    --dog-color: brown;
  }

  .dog {
    color: var(--dog-color);
  }
</style> 
```

## c) Interaction Markdown includes UI Lang
 
> uiliang is a minimal, ui-focused programming language for web designers.

> Create popovers, tabs, galleries, overlays and more using a language specifically designed for this. No programming experience is required.
 
👉 **[uilang.com](http://uilang.com/)**


---

⚠️ *TODO: Handling Pug inside of Lists, Quotes, Headlines etc*

