---
title: Html Tag
layout: default
excerpt: The html tag is the highest ranking Object within the Document Object Model ...
version: Page Template md Dtd 02-16-18
navigation_weight: 8
categories: template
---
# {{ page.title }}

{{ page.excerpt }}

{% include toc.md %}

## Html Box-node

The `html` tag, or ...

```html
{% raw %}
<html>...</html>
{% endraw %}
```

The html tag is the highest ranking Object within the **Document Object Model**, or [DOM](https://){:title='Document Object Model'}{:target='_blank'}.

The [DOM](https://){:title='Document Object Model'}{:target='_blank'} is derived from the many and varied tags and text found *nested* inside a single page of [Html](https://){:title='Hypertext Markup Language'}{:target='_blank'}.

For example, the `head` tag, or

```html
{% raw %}
<head>...</head>
{% endraw %}
```

Is *nested* within the `html` tag, or

```html
{% raw %}
<html>...</html>
{% endraw %}
```

Along with the `body` tag, or

```html
{% raw %}
<body>...</body>
{% endraw %}
```

As follows,

```html
{% raw %}
<html>
  <head>...</head>
  <body>...</body>
</html>
{% endraw %}
```

## Obfuscation

So, if we are presented with a `Box-node` by the [DOM](https://){:title='Document Object Model'}{:target='_blank'} after the browser *parses* your page of [Html](https://){:title='Hypertext Markup Language'}{:target='_blank'} ...

How then are we to find ...

- What `html` tag does the `Box-node` (parent) represent?

Or,

- What additional `Box-node` (child) or `Box-nodes` (siblings) does the `html` tag have *nested* within?

And,

- What `text` (leaves), if any, do these `Box-node` or `Box-nodes` contain?

## Global Variable

Inside the [DOM](https://){:title='Document Object Model'}{:target='_blank'}, the *Global Variable* takes on the name of **Document**.

The *Global Variable* through the name of **Document** grants us access to the [DOM](https://){:title='Document Object Model'}{:target='_blank'} Objects now representing the many and varied tags and text *parsed* from the underlying page of [Html](https://){:title='Hypertext Markup Language'}{:target='_blank'}.

For example,

The now **Document** has a `documentElement` property that refers to the [DOM](https://){:title='Document Object Model'}{:target='_blank'} Object that now represents the `html` tag.

In addition, the now **Document** also provides access to the now separate properties of `head` and `body`, both now representing the [DOM](https://){:title='Document Object Model'}{:target='_blank'} Objects derived from the *parsing* of the `head` and `body` tags over at the single page of [Html](https://){:title='Hypertext Markup Language'}{:target='_blank'}.

Got it?

## The DOM Root

The *root* of the parsed [Html](https://){:title='Hypertext Markup Language'}{:target='_blank'} page, as represented by the new [DOM](https://){:title='Document Object Model'}{:target='_blank'} is the new `document.documentElement` property.

The `document.documentElement` property points to the [DOM](https://){:title='Document Object Model'}{:target='_blank'} Object now representing the original `html` tag over at the now parsed single page of [Html](https://){:title='Hypertext Markup Language'}{:target='_blank'}.

## Node Properties

In addition, each new Object node within the newly constructed [DOM](https://){:title='Document Object Model'}{:target='_blank'} has a `nodeType` property that can be accessed.

The `nodeType` property returns a *numeral* representing which *type* of `node` the target `node` *is of* when queried.

### Constant type

The `constant` type of `node` is represented by the numeral one (1).

All *regular* elements of the [DOM](https://){:title='Document Object Model'}{:target='_blank'} tree return the numeral one (1) ...

And, are therefore of the `constant` type of `node`.

The *Document* Object property `document.ELEMENT_NODE` represents the `constant` type of `node`, or `constant` property.

### Leaf Type

All `text` nodes (leaves) of the **Document** Object return the numeral three (3) when queried by the `document.TEXT_NODE` property.

### Comment type

All `comment` nodes (leaves) of the **Document** Object return the numeral three (8) when queried by the `document.Comment_NODE` property.

## Parent nodes

Every `node` in the [DOM](https://){:title='Document Object Model'}{:target='_blank'} tree possesses a `parentNode` property from which the parent or *containing node* of the target `node` may be derived.

## Elemental Nodes

All *elemental* or *Type numeral one (1)* nodes of the [DOM](https://){:title='Document Object Model'}{:target='_blank'} Object also possess a `childNodes` property that can be accessed.

### Child Nodes

Every *Type numeral one (1)* or `elemental node` in the [DOM](https://){:title='Document Object Model'}{:target='_blank'} tree possesses a `childNodes` property from which the *array-like* object holding its children may be queried.

The `childNodes` property represents an array-like Object itself complete with a `length` property.

However, as a kind of the `NodeList` type, the `childNodes` property cannot be *sliced* as a regular array can be *sliced* through the `slice` method.

Nor can the `childNodes` property be accessed by the regular array method of `forEach`.

Array-like, yes.

But, not actually a full, regular array with the full compliment of properties and methods available to a regular array.

### First Child

**Note**. The value returned by the `firstChild` method is `null` when querying a `node` *sin niños*, or without children.

Similarly, the value returned by the `previousSibling` method is also `null` when querying a *primera niño*, or first child  `node`.

### Last Child

**Note**. The value returned by the `lastChild` method is `null` when querying a `node` *sin niños*, or without children.

Similarly, the value returned by the `nextSibling` method is also `null` when querying a *proxima niño final*, or next child last `node`.

## Document Body

As the spaces between tags over at the original single page of [Html](https://){:title='Hypertext Markup Language'}{:target='_blank'} convert to empty strings `""` when parsed by the browser to create the original [DOM](https://){:title='Document Object Model'}{:target='_blank'} ...

Querying the Object elements of the new [DOM](https://){:title='Document Object Model'}{:target='_blank'} by tag name is a more efficient procedure than attempting to pin point which `child` node where houses that one `leaf` node there.

For example, if you wish to extract the `href` portion of a hyperlink that was embedded in the original single page of [Html](https://){:title='Hypertext Markup Language'}{:target='_blank'} ...

That has since been been magically transported via the browser *parse* function over to the new [DOM](https://){:title='Document Object Model'}{:target='_blank'} Object, or *quasi-array* ...

By establishing a global variable named `link` and assigning the result of a procedure designed to *point* to all of the tags of the `a`, or *anchor* clan now resident in the [DOM](https://){:title='Document Object Model'}{:target='_blank'} via the hyperlink *quasi-array* Object ...

And, then *zeroing in* (literally) through the index feature of the *array-like* structure now representing the targeted `href` leaves ...

You may return an *array-like* [DOM](https://){:title='Document Object Model'}{:target='_blank'} Object that houses all of the hyperlinks that are descendants (either first as direct children, or secondly as indirect grand-children) of the index zero, or `[0]` hyperlink.

Finally, to render the result to the Javascript console, a friendly `console.log` invokation with the argument `(link.href)` attached will return the `href` portion you seek, as follows:

```html
{% raw %}
var link = document.body.getElementsByTagName("a")[0];
console.log(link.href)
{% endraw %}
```

**Note**. All *elemental* nodes possess a `getElementsByTagName` property in the form of a method that collects all targeted designated elements.

In this case the `getElementsByTagName` method collects all designated elements of the `a`, or *anchor* tag clan.

## Brackets Time

Now that we have a *snippet* of code to work with, let us now traverse over to our trusty instance of the Brackets IDE to see how our snippet renders.

After opening our `src` folder via the `file`, `open folder` selection of the Brackets IDE main menu ...

And, subsequently engaging the `Live Preview` feature of the Brackets IDE ...

We now see a rendering of our underlying single page of [Html](https://){:title='Hypertext Markup Language'}{:target='_blank'}.

Open up the Chrome browser tools and navigate to the `Sources`, `Snippets` tab of the main menu.

- Copy and paste the above two (2) lines of code into the `Snippets` window and save the snippet as `Get Element By Tag Name`

## Import Code

More to come ...

## Last Subtitle

**Note**. The above synopsis was derived from an article written by Blank [[2](#BLANK){:.red}].

### Raw Code Block

```liquid
{% raw %}
Enjoy the successful output!
{% endraw %}
```

{% include sources-and-uses.md %}

1. {:#BLANK}[The Blank Live at The Blank Festival, 2000](https://youtu.be/Blank){:title='Click to Watch the YouTube video of the Blank Live at the The Blank Festival, 2000'}{:target='_blank'}.

1. [Eloquent Javascript](https://www.syncfusion.com/resources/techportal/details/ebooks/eloquent-javascript){:title='Click to Visit the Landing page for Eloquent Javascript by Marijn Haverbeke at Synch Fusion dot com'}{:target='_blank'} by Marijn Haverbeke. Published by © 2012 [Syncfusion.com](https://www.syncfusion.com/){:title='Click to Visit the Home page of Synch Fusion dot com'}{:target='_blank'}.

1. [Jekyll Tips n Vids](https://learn.cloudcannon.com/){:title='Click to Visit the Landing page of Jekyll Tips n Vids by Cloud Cannon'}{:target='_blank'}. Published by © 2017 [Cloudcannon.com](https://www.cloudcannon.com){:title='Click to Visit the Home Page of Cloud Cannon dot com'}{:target='_blank'}.

### External Sources

- {:#SOURCELINKS}The [Project Source Links](https://mminail.github.io/Shell/Source-Shell-Links.htm){:title='Click to Visit the Source Links page of the Shell Lessons Project at Concepts Library'}{:target='_blank'} page of the Shell Lessons Project at Concepts Library. Published by © 2017 - 2018 [Mminail.github.io](https://mminail.github.io/){:title='Click to Visit the Home Page of the Concepts Library of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation'}{:target='_blank'}.

**Note**. This page crafted with {{ page.version }}.
