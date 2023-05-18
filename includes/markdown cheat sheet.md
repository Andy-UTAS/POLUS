# Markdown cheat sheet
Version 1.0, May 2023

In this Notebook, we'll go through some of the commands that help you format markdown (i.e. text) in your Jupyter Notebooks. Most of this you might not use, but it's handy nevertheless. Double click on the cells to open them up and see how the Markdown code works

# Headings 

Headings are made using the '#' symbol. By using multiple #s, you can create subheadings.

## Sub Heading

### Sub Sub Heading 

#### ..etc..

# Creating lists

Bullet points are created using - or *. Indenting the symbol created sub-lists etc...
* Something
    - Something else
        - More stuff
- Another thing

We make ordered lists using numbers
1. First thing
    1. Sub thing
        1. Other sub thing
2. Second thing

We can make check-box/task lists using square brackets: 
- [x] Have first coffee
- [ ] Have second coffee
- [ ] Have third coffee

# Changing text

We can make text **BOLD** or *italic* using the asterisk.

We can make indented quote blocks...
> In the beginning...etc...

We can also highlight code operations in-text by encasing the text like so: `code/function/thing`

Or used fenced code blocks...

```
Code thing
does some stuff 
```

We can highlight regular text using HTML tags...
<mark>Highlighted Text</mark>

<mark style="background-color: lightgreen">Or in a different color</mark>


<span style="color:orange">Changing text color is a similar process</span>

# Equations

Rather than typing our equations out like E=mc^2, we can format them using `$`. We can format them in line with our text using one set of `$s`, i.e. $E=mc^2$. Or we can make them stand out on the page with a double set `$$`...
$$E=mc^2.$$ 

If we want superscripts and subscripts e.g. $x_2, x^2$. If there are multiple things in a subscript or superscript then we use curly brackets `x^{7t-3}_{a,b,c}` $$x^{7t-3}_{a,b,c}$$

Sometimes it is necessary to format mathematical expressions over multiple lines, and formatting in these situations should be done using the align environment.

$$
    \begin{align}
        V_{in} & =V_C+V_R \\
        & = \frac{q}{C} + IR
    \end{align}
$$

We use the `\` a lot to enter math commands... 
- If we want fractions $\frac{2}{3}$. 
- If we want some Greek letters $\alpha, \beta, \mu, \gamma, \Gamma, \eta, \theta, \Theta$
- If we want some basic operations $\times, \div, \nabla, \int, \ln, \log, \ne, \sim, \gtrsim, \lesssim, \gg, \ll, \iff$
- Change the size of an equation with `\small, \large, \Large, \huge, \Huge` e.g. $$\Huge{x+2}$$$$\huge{x+2}$$$$\Large{x+2}$$$$\large{x+2}$$$$\small{x+2}$$

# Inserting Links 

Inserting links to stuff on the internet is useful when you want to remember where you got information from. It works like this:

`[title](https://www.example.com)`

For example, here is the Wikepedia page about [Cats](https://en.wikipedia.org/wiki/Cat)

# Tables

When constructing tables, you draw the table in using combinations of '|' and '--' as seen here.

| Thing | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |

# Images

Images can be imported via

`![image](path/to/image.svg)`

![](puppy.jpg)


## Adding a caption
Adding captions to images isn't quite as straightforward, but can be done using

```
<figure>
    <img src="path/to/image.svg">
    <figcaption> Caption </figcaption>
</figure>
```

<figure>
    <img src="puppy.jpg">
    <figcaption> Who's a good boi </figcaption>
</figure>