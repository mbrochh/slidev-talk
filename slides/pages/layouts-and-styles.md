---
layout: two-cols
title: Layouts & Styles
---

<style>
  .col-left {
    padding-right: 1em;
  }
</style>

# Layouts & Styles

```md
---
layouts: two-cols
---

<style>
  .col-left {
    padding-right: 1em;
  }
</style>

# Slide Headline 

- some content here

::right::

<h1>&nbsp;</h1>

- some content here

```

::right::

<h1>&nbsp;</h1>

- the `<style>` block adds some padding to the left column
- use the inspect tool to find the class names when writing custom styles
- the `::right::` block marks the end of the left column
- the `<h1>` tag is a hack to make the right column content start at the same height as the left column content
- lean more about layouts here: [https://sli.dev/builtin/layouts.html](https://sli.dev/builtin/layouts.html)

