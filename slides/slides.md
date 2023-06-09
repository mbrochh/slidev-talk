---
theme: default
background: https://source.unsplash.com/collection/94734566/1920x1080
class: 'text-center'
highlighter: shiki
lineNumbers: true
title: Slidev for Tech Talks
drawings:
  persist: false
transition: fade
css: unocss
---

# Slidev for Tech Talks

A quick introduction to making slides with Slidev

by [Martin Brochhaus](https://twitter.com/mbrochh)

---
src: ./pages/about-me.md
---

---
src: ./pages/about-pugs.md
---

---

# Read The Docs!

- [https://sli.dev/guide/](https://sli.dev/guide/)

<img src="/images/slidev-docs.png" class="w-full mt-3" />

---

# Setup

- Create a git repo
- Create `README.md`
- Create `initial commit`
- `git remote add origin git@github.com:YOURNAME/YOUR-REPO.git`
- `git push -u origin master`
- `npm init slidev`
- `cd slidev`
- `npm run dev`

---

# Slides Metadata

- replace the content of the `slides.md` file with this:

```md
---
theme: default
background: https://source.unsplash.com/collection/94734566/1920x1080
class: 'text-center'
highlighter: shiki
lineNumbers: true
title: [YOUR TALK TITLE HERE]
drawings:
  persist: false
transition: fade
css: unocss
---
```

---

# The Cover Slide

- The first slide after the metadata is the cover slide
- right after the metadata, add this:

```md {4-12}
---
... metadata at the top of the file here
---

# YOUR TALK TITLE HERE

YOUR TALK SUBTITLE HERE


by [YOUR NAME](https://twitter.com/YOUR_TWITTER_HANDLE)

---
```

---

# The About Slide

- You will probably have some slides that you need in all of your talks
- Create files inside the `pages/` folder:

```md {2-10}
... ealier content here

---
src: ./pages/about-me.md
---

---
src: ./pages/about-pugs.md
---

---

# Next normal slide here

---
```

- Note the empty lines around the `---`

---
src: ./pages/layouts-and-styles.md
---

---

# Clicks For Lists

- If you have a list in Markdown, you can use `<v-clicks>` to show the list items one by one

```md
<v-clicks>

- first item
- second item

</v-clicks>

```

<br />

### Example:

<v-clicks>

- first item
- second item

</v-clicks>

---
clicks: 3
---

# Clicks For Custom Elements

- You can also use `<v-clicks>` for custom elements

```md
---
clicks: 3
---

<div v-click="1">Element 1</div>
<div v-click="3">Element 3</div>
<div v-click="2">Element 2</div>
```

<br />

### Example:

<div v-click="1">Element 1</div>
<div v-click="3">Element 3</div>
<div v-click="2">Element 2</div>


---

# Code highlights

- the coolest thing about Slidev is the code highlighting
- you can highlight single lines or ranges of lines

```md
    ```py {1,3-4}
    import os, sys
    # darker line
    print("Hello World")
    sys.exit(0)
    ```
```

<br />

```py {1,3-4}
import os, sys
# darker line
print("Hello World")
print("Foobar")
sys.exit(0)
```

---

# Long Code Blocks

- if you have a long code block, it will add scroll barso

```md
    ```py {all} {maxHeight: '100px'}
    print(1)
    print(2)
    print(3)
    print(4)
    print(5)
    print(6)
    print(7)
    print(8)
    print(9)
    ```
```

<br />

### Example:

```py {all} {maxHeight: '100px'}
print(1)
print(2)
print(3)
print(4)
print(5)
print(6)
print(7)
print(8)
print(9)
```

---

# Images

- just place images into the `public/` folder
- use TailwindCSS to style the image

```html
<img src="/images/membership.png" class="w-[200px] m-auto mt-4" />
```

<br />

### Example:

<img src="/images/membership.png" class="w-[200px] m-auto mt-4"  />

---

# Awesome Controls

- hover with the mouse to the bottom left corner

<img src="/images/controls.png" class="w-full mt-4" />

---

# Publishing The Slides

- change `build` command in `package.json` 

```json
"build": "slidev build --base /REPO-NAME",
```

<v-clicks>

- run `npm run build`, this will create a `dist/` folder
- run `mv dist ../docs`, this will move the build to the `docs/` folder at the project root
- `git add .` - add all files to git
- `git commit` - write your commit message
- `git push` - push to GitHub
- browse to `https://github.com/YOURNAME/YOUR-REPO/settings/pages`
- select `master` branch and `/docs` folder and click `Save`
- browse to `https://YOURNAME.github.io/YOUR-REPO/`

</v-clicks>


---
layout: end
---
