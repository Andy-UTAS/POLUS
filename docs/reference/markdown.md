# Markdown

[Markdown](https://en.wikipedia.org/wiki/Markdown) is a _[markup language](https://en.wikipedia.org/wiki/Markup_language)_ which can be used to simply and beautifully format text^[1], with a major advantage being that even when it is not rendered, it is easily readable by humans, unlike say, HTML. Another advantage to many in the sciences is that when one is using [Jupyter](../computation#using-python) notebooks to program in `python`, one can use `markdown` to embed formatted text in the notebook, making the code eminently readable. Indeed, it is for this reason that [experimental logbooks are required to be prepared using markdown](reference/experiment/#model-log-book).

Provided below are some tips and tricks for preparing `markdown` content, but there are countless excellent resources[^2] on the web for learning markdown, so you are encourage to look around.

![](markdown/header.jpg){: .center}

---

## How do I markdown?

Writing markdown is not particularly difficult once one knows the tricks of the trade. Perhaps the biggest step one must take is recognising that difference between a text editor and a program for rendering text. A text editor is simple, for example, _Notepad_ for Windows is a very simple text editor with no frills and allows one to simply write text, and importantly also code. The difference between text and code is that text is designed to be digested by humans, whereas code is to be digested by an interpreter (in essence, the computer). However, in practice when it comes to actually reading and digesting text, the display of text editors is typically visually unappealing and often difficult to read. One solution is to create a text editor which renders text into a better format in real time, such as Microsoft Word, but as anyone who has spent any time with Word, it has limitations when it comes to usability and formatting. In the world of science, especially when it comes to publishing, it is much more convenient to use tools such as markdown or [$\LaTeX$](https://en.wikipedia.org/wiki/LaTeX) which allow the user to write pseudo-code, where content is written in an editor, and then compiled prior to consumption, where the compiler renders the text, images, and other objects (e.g. code, tables, etc.) to make everything look pretty. The answer to the question "how do I markdown" is thus write pseudo code in an editor of your choice and then compile it. Which editor should you use? Well, [free and open-source editors exist online](https://stackedit.io/app#) and these can be great for getting a start, or you can write markdown in [Jupyter](../computation/#using-python) as described elsewhere.

## This page

This page has a sole purpose: to serve as a reference page for common markdown functions.

### Markdown cheat sheet
[<i class="fab fa-markdown fa-5x"></i>](https://jove2021.cloud.edu.au/ "Github of rendered markdown"){ .md-button .md-button--primary class="text-center" style="margin-left: 21.5%"}
[<i class="fab fa-github fa-5x"></i>](https://jove2021.cloud.edu.au/ "Github of markdown code"){ .md-button .md-button--primary class="text-center" style="margin-left: 7.5%"}
[<i class="fab fa-python fa-5x"></i>](https://github.com/Andy-UTAS/POLUS/blob/master/docs/reference/experiment/model_log/examplelog.ipynb "Markdown on Jove"){ .md-button .md-button--primary class="text-center" style="margin-left: 7.5%"}

The cheat sheet is best viewed on this site, as it shows both the markdown code and rendered outcome, but you can also access the raw markdown or pure rendered form of this cheat sheet on GitHub, or access a Jupyter notebook of the markdown to experiment yourself.

---

## Markdown cheat sheet

### Formatting

#### Headings

Headings are made using the `#` symbol. By using multiple `#` symbols, you can create subheadings.

``` markdown title="Using headings"

# Heading

## Sub Heading

### Sub Sub Heading

#### ..etc..
```
<div class="result" markdown>
<br>
# Heading
## Sub Heading
### Sub Sub Heading
#### ..etc..
</div>

#### Lists

##### Unordered lists

Bullet points are created using `-` or `*`. Indenting the symbol created sub-lists etc...

``` markdown title="Unordered lists"
* Something

    - Something else

        - More stuff

- Another thing
```
<div class="result" markdown>
* Something

    - Something else

        - More stuff

- Another thing
</div>

##### Ordered lists

We make ordered lists using numbers

``` markdown title="Ordered lists"
1. First thing

    1. Sub thing

        1. Other sub thing

2. Second thing
```
<div class="result" markdown>
1. First thing

    1. Sub thing

        1. Other sub thing

2. Second thing
</div>

##### Task lists

We can make check-box/task lists using square brackets:
``` markdown title="Task lists"
- [x] Have first coffee
- [ ] Have second coffee
- [ ] Have third coffee
```
<div class="result" markdown>
- [x] Have first coffee
- [ ] Have second coffee
- [ ] Have third coffee
</div>

#### Text

##### Emphasis
``` markdown title="Text accentuation"
We can make text **BOLD** or *italic* using the asterisk.
```
<div class="result" markdown>
We can make text **BOLD** or *italic* using the asterisk.
</div>

##### Quote blocks
Indented quation blocks can be created using `>`
``` markdown title="Quote blocks"
> In the beginning...etc..
```
<div class="result" markdown>

> In the beginning...etc..

</div>

##### Code
We can also highlight code operations inline by encasing the text using the `` ` `` or creating code blocks using `` ``` ``

```` markdown title="Coding"
Inline code can be rendered using `code/function/thing` whilst code blocks are created via

```
Code thing
does some stuff
```

````
<div class="result" markdown>
Inline code can be rendered using `code/function/thing` whilst code blocks are created via

```
Code thing
does some stuff
```
</div>

##### Accentuation

We can highlight regular text using HTML tags...

``` markdown title="Colouring text"
<mark>Highlighted Text</mark>

<mark style="background-color: lightgreen">Or in a different color</mark>

<span style="color:orange">Changing text color is a similar process</span>
```
<div class="result" markdown>
<mark>Highlighted Text</mark>

<mark style="background-color: lightgreen">Or in a different color</mark>

<span style="color:orange">Changing text color is a similar process</span>
</div>

#### Equations

##### Typesetting

Rather than typing our equations out like E=mc^2, we can format them using `$`. We can format them inline with our text using a set of `$`, or we can make them stand out on the page with a double set `$$`

``` markdown title="Equations"
$E=mc^2$ will render an inline equation. Using `$$` will make an equation block:

$$
E=mc^2
$$
```
<div class="result" markdown>
$E=mc^2$ will render an inline equation. Using `$$` will make an equation block:

$$
E=mc^2
$$
</div>

##### Sub- and superscripts

If we want superscripts and subscripts, we can use `^` and `_` whilst in `math` mode, that is, in a `$` environment.

``` markdown title="Superscripts and subscripts"
Subscripts and superscripts are created using $x_2, x^2$. If there are multiple characters in a subscript or superscript, curly braces must be used. For example, compare

$$
x^(7t-3)_(a,b,c)
$$

to

$$
x^{7t-3}_{a,b,c}
$$


```
<div class="result" markdown>

Subscripts and superscripts are created using $x_2, x^2$. If there are multiple characters in a subscript or superscript, curly braces must be used. For example, compare

$$
x^(7t-3)_(a,b,c)
$$

to

$$
x^{7t-3}_{a,b,c}
$$
</div>

##### Multiline equations

Sometimes it is necessary to format mathematical expressions over multiple lines, and formatting in these situations should be done using the `align` environment.

``` markdown title="Multiline equations"
$$
    \begin{align}
        V_{in} & =V_C+V_R \\
        & = \frac{q}{C} + IR
    \end{align}
$$
```

<div class="result" markdown>
$$
    \begin{align}
        V_{in} & =V_C+V_R \\
        & = \frac{q}{C} + IR
    \end{align}
$$
</div>

##### Special characters
We use the `\` a lot to enter math commands...
``` markdown title="Special characters and commands"
- If we want fractions $\frac{2}{3}$.
- If we want some Greek letters $\alpha, \beta, \mu, \gamma, \Gamma, \eta, \theta, \Theta$
- If we want some basic operations $\times, \div, \nabla, \int, \ln, \log, \ne, \sim, \gtrsim, \lesssim, \gg, \ll, \iff$
- Change the size of an equation with `\small, \large, \Large, \huge, \Huge` e.g.
$$\small{x+2}$$
$$\large{x+2}$$
$$\Large{x+2}$$
$$\huge{x+2}$$
$$\Huge{x+2}$$
```
<div class="result" markdown>
- If we want fractions $\frac{2}{3}$.
- If we want some Greek letters $\alpha, \beta, \mu, \gamma, \Gamma, \eta, \theta, \Theta$
- If we want some basic operations $\times, \div, \nabla, \int, \ln, \log, \ne, \sim, \gtrsim, \lesssim, \gg, \ll, \iff$
- Change the size of an equation with `\small, \large, \Large, \huge, \Huge` e.g.
$$\small{x+2}$$
$$\large{x+2}$$
$$\Large{x+2}$$
$$\huge{x+2}$$
$$\Huge{x+2}$$
</div>

### Functionality

#### Hyperlinks
Inserting links to stuff on the internet is useful when you want to remember where you got information from. It works using a combination of brackets and parentheses `[]()` with the following syntax `[title](link)`.

``` markdown title="Inserting links"
[Here](https://en.wikipedia.org/wiki/Cat) is the Wikepedia page about cats
```
<div class="result" markdown>
[Here](https://en.wikipedia.org/wiki/Cat) is the Wikepedia page about cats
</div>

#### Tables
When constructing tables, you draw the table in using combinations of `|` and `--` as seen here.

``` markdown title="Inserting a table"
| Thing | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
```
<div class="result" markdown>
| Thing | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
</div>


### Images

Images can be imported via

``` markdown title="Place an image"
![image](path/to/image.svg)
```


<div class="result" markdown>

![](markdown/puppy.jpg){: .center}

</div>

#### Adding a caption

Adding captions to images isn't quite as straightforward, but can be done using

``` markdown title="Place an image with a caption"
<figure>
    <img src="path/to/image.svg">
    <figcaption> Caption </figcaption>
</figure>
```

<div class="result" markdown>

<figure>
    <img src="puppy.jpg">
    <figcaption> Who's a good boi </figcaption>
</figure>

</div>

[^1]: This entire site is (mostly) written using markdown!
[^2]: The [_Markdown Guide_](https://www.markdownguide.org/) is an excellent example
