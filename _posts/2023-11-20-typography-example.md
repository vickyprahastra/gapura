Content, and content marketing, is critical today. Sometimes, though, the systems to create content get in the way, overwhelming users and offering too many options.

## Headings

Headings from `h1` through `h6` are constructed with a `#` for each level:

# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading

```markdown
# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading
```

## Horizontal Rules

The HTML `<hr>` element is for creating a "thematic break" between paragraph-level elements. In markdown, you can create a `<hr>` with any of the following:

* `___`: three consecutive underscores
* `---`: three consecutive dashes
* `***`: three consecutive asterisks

## Emphasis

### Bold
For emphasizing a snippet of text with a heavier font-weight.

**rendered as bold text**

```markdown
**rendered as bold text**
```
### Italics
For emphasizing a snippet of text with italics.

_rendered as italicized text_

```markdown
_rendered as italicized text_
```

### Strike through

~~Strike through this text.~~

```markdown
~~Strike through this text.~~
```

## Blockquotes
For quoting blocks of content from another source within your document.

`Quote text`

```markdown
`Quote text`
```

## Lists

### Unordered
A list of items in which the order of the items does not explicitly matter.

You may use any of the following symbols to denote bullets for each list item:

### Unordered

* Lorem ipsum dolor sit amet
* Consectetur adipiscing elit
* Integer molestie lorem at massa
* Facilisis in pretium nisl aliquet
* Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
  - Vestibulum laoreet porttitor sem
  - Ac tristique libero volutpat at

+ Faucibus porta lacus fringilla vel
+ Aenean sit amet erat nunc
+ Eget porttitor lorem

```markdown
* Lorem ipsum dolor sit amet
* Consectetur adipiscing elit
* Integer molestie lorem at massa
* Facilisis in pretium nisl aliquet
* Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
  - Vestibulum laoreet porttitor sem
  - Ac tristique libero volutpat at

+ Faucibus porta lacus fringilla vel
+ Aenean sit amet erat nunc
+ Eget porttitor lorem
```

### Ordered

1. Start with a number
1. Consectetur adipiscing elit
1. Integer molestie lorem at massa
1. Facilisis in pretium nisl aliquet
1. Nulla volutpat aliquam velit
1. Faucibus porta lacus fringilla vel
1. Aenean sit amet erat nunc
2. Eget porttitor lorem

```markdown
1. Start with a number
1. Consectetur adipiscing elit
1. Integer molestie lorem at massa
1. Facilisis in pretium nisl aliquet
1. Nulla volutpat aliquam velit
1. Faucibus porta lacus fringilla vel
1. Aenean sit amet erat nunc
2. Eget porttitor lorem
```

## Code

### Inline code

```
Look at this ```Inline code here...``` :)
```

### Indented code

Or indent several lines of code by at least four spaces, as in:

```
    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
```

### Block code "fences"

Use "fences"  ```` ``` ```` to block in multiple lines of code.

    ```
    Sample text here...
    ```


### Syntax highlighting
Add the file extension of the language you want to use directly after the first code "fence" and syntax highlighting will automatically be applied in the rendered HTML. For example, to apply syntax highlighting to JavaScript code:



```js
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```



## HTML blocks
HTML blocks (e.g. div, table, pre, p) must be separated from surrounding content by blank lines and the start and end of the block should not be indented with tabs or spaces

```markdown
**Bold** text

<div>
  **Bold** text
</div>

**Bold** text
```

## Tables
Tables are created by adding pipes as dividers between each cell, and by adding a line of dashes (also separated by bars) beneath the header. Note that the pipes do not need to be vertically aligned.

```markdown
  | Option | Description |
  | ------ | ----------- |
  | data   | path to data files to supply the data that will be passed into templates. |
  | engine | engine to be used for processing templates. Handlebars is the default. |
  | ext    | extension to be used for dest files. |
```


### Aligned text

Adding a colon on the right side of the dashes below any heading will right align text for that column.

```markdown
| Option | Type    | Description |
| :------| :-----: | -----------:|
| data   | text    | path to data files to supply the data that will be passed into templates. |
| engine | text    | engine to be used for processing templates. Handlebars is the default. |
| ext    |  text   | extension to be used for dest files. |
```

## Links and Images

### Basic link

[Example](http://example.com)

```markdown
[Example](http://example.com)
```

### With a title
[Vicky](https://vicky.prahastra.com "Example")

```markdown
[Vicky](https://vicky.prahastra.com "Example")
```

### Images
Images have a similar syntax to links but include a preceding exclamation point.

![Minion](/assets/images/profilepicture.png)
![Alt text](/assets/images/profilepicture.png "The Image")

```markdown
![Minion](http://image.com/path/to/image.png)
```

```markdown
![Alt text](http://example.com/path/to/image.png "The Image")
```

### Footnote style

![Alt text][image]
[Vicky Prahastra][link]

[image]: /assets/images/profilepicture.png  "The Image"
[link]: https://vicky.prahastra.com "Vicky Prahastra"

```markdown
![Alt text][image]
[Example][link]

[image]: /assets/images/profilepicture.png  "The Image"
[link]: https://vicky.prahastra.com "Vicky Prahastra"
```
