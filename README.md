# introduction-to-html-assignment

## What is HTML?
HTML is the language used to create the websites you visit everyday. It provides a logical way to structure content for websites. Let's analyze the acronym "HTML," as it contains a lot of useful information. HTML stands for HyperText Markup Language.

A **markup language** is a computer language that defines the structure and presentation of raw text. Markup languages work by surrounding raw text with information the computer can interpret, "marking it up" to be processed.

In HTML, the computer can interpret raw text that is wrapped in HTML elements. These elements are often nested inside one another, with each containing information about the type and structure of the information to be displayed in the browser.

**HyperText** is text displayed on a computer or device that provides access to other text through links, also known as “hyperlinks.” In fact, you probably clicked on many, many hyperlinks on your path to this Codecademy course!

## Instructions for Assignment
In this assignment you will familiarize yourself with HTML by creating a simple web site. Once you have cloned this repository to your classroom Raspberry Pi create a file called `index.html` and open it up using the nano text editor.

### Step 1: Set up
- [ ] Open up a tab in the chromium web browser and open up the file `index.html` (press CTRL-O). In your `index.html` file, type in `<h1> </h1>` and type in your name in between `<h1>` and `</h1>`. Save the file in nano and reloade the page in the browser. What do you notice? Commit your file with an appropriate log message and push to GitHub.

### Step 2: `<!DOCTYPE html>`
Whether you realize it or not, when you read text, your brain must first identify the text's language. If you can understand that language, then your brain immediately begins to interpret the text. This same process happens whether you're reading a street sign, a book, or a name tag. Web browsers work in a similar way. They must know what language a document is written in before they can process its contents.

You can let web browsers know that you are using HTML by starting your document with a document type declaration.

The declaration looks like this: `<!DOCTYPE html>`. This declaration is an instruction. It tells the browser what type of document to expect, along with what version of HTML is being used in the document.

`<!DOCTYPE html>` must be the first line of code in all of your HTML documents. If you don't use the declaration, your HTML code will likely still work, however, it's risky. For now, the browser will correctly assume that the html in `<!DOCTYPE html>` is referring to HTML5, as it is the current standard.

In the future, however, a new standard will override HTML5. Future browsers may assume you're using a different, newer standard, in which case your document will be interpreted incorrectly. To make sure your document is forever interpreted correctly, always include `<!DOCTYPE html>` at the very beginning of your HTML documents.

- [ ] Add `<!DOCTYPE html>` as the first line in your HTML file.

### Step 3: Preparing for HTML
The `<!DOCTYPE html>` declaration is only the beginning, however. It indicates to the browser that you will use HTML in the document, but it doesn't actually add any HTML structure or content.

To create HTML structure and content, we must add opening and closing `<html>` tags, like so:
```
<!DOCTYPE html>
<html>

</html>
```
Anything between the opening `<html>` and closing `</html>` tags will be interpreted as HTML code. Without these tags, it's possible that browsers could incorrectly interpret your HTML code.

- [ ] After the `<!DOCTYPE html>` declaration add the opening (`<html>`) and closing (`</html>`) HTML tags.

### Step 4: HTML Anatomy
Before we move forward, it's important that we discuss how HTML elements are structured. A simple example to illustrate this is the following HTML code:
```
<p>Hello world</p>
```
In this example, the paragraph element is made up of one opening tag (`<p>`), the “Hello world!” text, and a closing tag (`</p>`):

Let's quickly review each part of the tag pictured:
* HTML Tag - The element name, surrounded by an opening (`<`) and closing (`>`) angle bracket.
* HTML element (or simply, element) - a unit of content in an HTML document formed by HTML tags and the text or media it contains.
* Opening tag - the first HTML tag used to start an HTML element. The tag type is surrounded by opening and closing angle brackets.
* Element content - The information (text or other elements) contained between the opening and closing tags of an HTML element.
* Closing tag - the second HTML tag used to end an HTML element. Closing tags have a forward slash (`/`) inside of them, directly after the left angle bracket.

Most elements require both opening and closing tags, but some call for a single self-closing tag. We will encounter examples of both element types in the next few exercises.

### Step 4: The Head
So far you've done two things:
1. Declared to the browser that your code is HTML.
2. Added the HTML element (<html>) that will contain the rest of your code.

Let's also give the browser some information about the page. We can do this by adding a `<head>` element. The `<head>` element contains the metadata for a web page. Metadata is information about the page that isn't displayed directly on the web page. You'll see an example of this in the next exercise. The opening and closing head tags (`<head></head>`) typically appear as the first item after your first HTML tag.

- [ ] Add the opening and closing `<head>` and `</head>` tags between the opening and closing `<html>` tags.

### Step 5: Page Titles
What kind of metadata about the web page can the `<head>` element contain? If you navigate to any webpage and look at the top of your browser (or at the tab you have open), you'll notice the it has a title. The browser displays the title of the page because the title can be specified directly inside of the `<head>` element, by using a `<title>` tag.
```
<!DOCTYPE html>
<html>
  <head>
    <title>My Coding Journal</title>
  </head>
</html>
```
If we were to open a file containing the HTML code in the example above, the browser would display the words My Coding Journal in the title bar (or in the tab's title).

- [ ] Add a title to your web page using the `<title>` element. The title should say `The poetry of Shakespear`. Reload the web page and your title should appear in the title bar.

### Step 6: The Body
We've added some HTML, but still haven't seen any results in the web browser to the right. Why is that? Before we can add content that a browser will display, we have to add a body to the HTML file. Only content inside the opening and closing body tags can be displayed to the screen.

Once the file has a body, many different types of content – including text, images, and buttons – can be added to the body.

```
<!DOCTYPE html>
<html>
  <head>
    <title>I'm Learning To Code!</title>
  </head>
  <body>

  </body>
</html>
```

In the example above, the opening body tag (`<body>`) is placed directly below the closing head tag (`</head>`), and the closing body tag (`</body>`) is placed directly above the closing html tag (`</html>`).

- [ ] Add a body to your web page using the `<body>` element and add the following code between your opening and closing body tags: `<p>Shall I compare thee to a summer's day? Thou art more lovely and more temperate</p>`

### Step 7: Self-closing Tag
Thus far we have only seen HTML elements with an opening and a closing tag. A few types of elements, however, require only one tag. Self-closing elements contain all the information the browser needs to render the element inside a single tag. Also, because they are single tags, they cannot wrap around raw text or other elements. The line break element `<br />` is one example of a self-closing tag. You can use it anywhere within your HTML code. The result is a line break in the browser.

```
<p>line one<br />line two</p>
```

In the example above, the paragraph tags (`<p>`) enclose two phrases, split by a break tag (`<br />`). Note that single tags, unlike elements with two tags, can't wrap around raw text or other elements.

The code in the example above will result in an output that looks like the following:

```
line one
line two
```
Without the break tag, the browser would render line one and line two on the same line.

- [ ] Add a self-closing `<br />` tag after the question mark `?`.

### Step 8: HTML Structure
The rest of this assignment will focus on how HTML is structured and some tools developers use to make code easier to interpret. HTML documents are organized as a collection of parent-child relationships. When an element is contained inside another element, it is considered the child of that element. The child element is said to be nested inside of the parent element.

```
<body>
  <p>Paragraph</p>
</body>
```
In the example above, the `<p>` element is nested inside the `<body>` element. The `<p>` element is considered a child of the `<body>` element, the parent. Since there can be multiple levels of nesting, this analogy can be extended to grandchildren, great-grandchildren and beyond. Let's consider a more complicated example:

```
<body>
  <div>
    <h1>Student</h1>
    <p>Get Started</p>
  </div>
</body>
```

In this example, the `<body>` element is the parent of the `<div>` element. Both the `<h1>` and `<p>` elements are children of the `<div>` element. Because the `<h1>` and `<p>` elements are in the same level, they are considered siblings, and are both grandchildren of the `<body>` element. Understanding this hierarchy is important, because child elements can inherit attributes from their parent element.

- [ ] Create a div element where the paragraph you have on your web page is a child of the div element. Add the heading `<h1>Shall I compare thee to a summer’s day? (Sonnet 18)</h1>` as a child of the body element.

### Step 9: Whitespace
As the code in an HTML file grows, it becomes increasingly difficult to keep track of how elements are related. Programmers use two tools to visualize the relationship between elements: whitespace and indentation. Both tools take advantage of the fact that the position of elements in a browser is independent of the amount of whitespace or indentation in the `index.html` file.

For example, if you wanted to increase the space between two paragraphs on your web page, you would not be able to accomplish this by adding space between the paragraph elements in the `index.html` file. The browser ignores whitespace in HTML files when it renders a web page, so it can be used as a tool to make code easier to read and follow.

What makes the example below difficult to read?

```
<body><p>Paragraph 1</p><p>Paragraph 2</p></body>
```
You have to read the entire line to know what elements are present. Compare the example above to this:

```
<body>
<p>Paragraph 1</p>
<p>Paragraph 2</p>
</body>
```
This example is easier to read, because each element is on its own line. While the first example required you to read the entire line of code to identify the elements, this example makes it easy to identify the body tag and two paragraphs.

A browser renders both examples the same way:

```
Paragraph 1
Paragraph 2
```
- [ ] Replace the paragraph you currently have with the following HTML code, making sure you use whitespace to make the code more readable by putting each element on its own line. 

```
<p>Shall I compare thee to a summer’s day? <br />Thou art more lovely and more temperate.<br />Rough winds do shake the darling buds of May,<br />And summer’s lease hath all too short a date.<br /></p></p>Sometime too hot the eye of heaven shines,<br />And often is his gold complexion dimmed;<br />And every fair from fair sometime declines,</p><p>By chance, or nature’s changing course, untrimmed;<br />But thy eternal summer shall not fade,<br />Nor lose possession of that fair thou ow’st,<br />Nor shall death brag thou wand’rest in his shade,</p><p>When in eternal lines to Time thou grow’st.<br />So long as men can breathe, or eyes can see,<br />So long lives this, and this gives life to thee.</p>
```

### Step 10: Indentation
The second tool web developers use to make the structure of code easier to read is indentation. The World Wide Web Consortium, or W3C, is responsible for maintaining the style standards of HTML. At the time of writing, the W3C recommends 2 spaces of indentation when writing HTML code. Although your code will work without exactly two spaces, this standard is followed by the majority of professional web developers. Indentation is used to easily visualize which elements are nested within other elements.
```
<body>
  <p>Paragraph 1</p>
  <div>
    <p>Paragraph 2</p>
  </div>
</body>
```
In the example above, Paragraph 1 and the `<div>` tag are nested inside of the `<body>` tag, so they are indented two spaces. The Paragraph 2 element is nested inside of the `<div>` tag, so it is indented an additional two spaces. The spaces are inserted using the spacebar on your keyboard.

- [ ] Indent your code in `index.html` to match the W3C standards.

### Step 11: Comments
HTML files also allow you to add comments to your code.

Comments begin with `<!-- and end with -->`. Any characters in between will be ignored by your browser. For example,
```
<!-- This is a comment that the browser will not display. -->
```
Including comments in your code is helpful for many reasons:
* They help you (and others) understand your code if you decide to come back and review it at a much later date.
* They allow you to experiment with new code, without having to delete old code.

```
<!-- Favorite Films Section -->
<p>The following is a list of my favorite films:</p>
```
In this example, the comment is used to denote that the following text makes up a particular section of the page.

```
<!-- <p> Test Code </p> -->
```

In the example above, a valid HTML element (a paragraph element) has been "commented out." This practice is useful when there is code you want to experiment with, or return to, in the future.

- [ ] Add at least one comment to ```index.html``` explaining the purpose of the code.

### Step 12: Headings
Headings in HTML can be likened to headings in other types of media. For example, in newspapers, large headings are typically used to capture a reader's attention. Other times, headings are used to describe content, like the title of a movie or an educational article. HTML follows a similar pattern. In HTML, there are six different headings, or heading elements. Headings can be used for a variety of purposes, like titling sections, articles, or other forms of content.

The following is the list of heading elements available in HTML. They are ordered from largest to smallest in size.

* `<h1>` - used for main headings. All other smaller headings are used for subheadings.
* `<h2>`
* `<h3>`
* `<h4>`
* `<h5>`
* `<h6>`
The following example code uses a headline intended to capture a reader's attention. It uses the largest heading available, the main heading element:

```
<h1>BREAKING NEWS</h1>
```

- [ ] In `index.html`, add an `<h1>` heading under the opening body tag. The heading should say: Poems by William Shakespeare, change the existing h1-level heading to a h2-level heading and add another h2-level heading below the h1-level heading. The new headings should say: All the worlds a stage.

### Step 13: Text Content Tags
Headings are meant to emphasize or enlarge only a few words. If you want to add blocks of text in HTML, you can use a paragraph, div, or span:
* Paragraphs (`<p>`) simply contain a block of plain text.
* `<div>`s can contain any text or other HTML elements. They are primarily used to divide HTML documents into sections.
* `<span>`s contain short pieces of text or other HTML. They are primarily used to wrap small pieces of content that are on the same line as other content and do not break text into different sections.

Take a look at each of these elements in action below:
```
<div>
    <p>Technology</p>
</div>
<div>
  <p><span>Self-driving cars</span> are anticipated to replace up to 2 million jobs over the next two decades.</p>
</div>
```
In the example above, there are two different `<div>`s that each contain `<p>` elements. The second <div> contains a `<p>` with `<span>`Self-driving cars`</span>`. This `<span>` element separates Self-driving cars from the rest of the text in the paragraph. As we noted above, the `<div>`s divided blocks of code, while the `<span`> divides inline text, or text that is on the same line as other text.

Below, we're going to add several `<div>`s with ids to organize our text into sections. Later, we will use this structure to create links that allow a user to quickly navigate the content of our page.

Note: We will explain the purpose of the ids that you will see in a later exercise. An id only needs to be in the opening tag of an element.

- [ ] Below the `<h1>` element that says Poems by William Shakespeare, add this opening `<div>` tag: `<div id="introduction">`. Add the closing `</div>` tag after the `<h2>` element that says All the worlds a stage. Always add two spaces of indentation when you nest elements inside of `<div>`s.

- [ ] Below the `<h2>` element that says All the worlds a stage, add a paragraph that is indented the same amount of space as the other content inside of this `<div>`. The paragraph should contain the following text:
```
All the world's a stage, And all the men and women merely players;
They have their exits and their entrances,
And one man in his time plays many parts,
His acts being seven ages.
```

### Step 14: Text Style Tags
Tags provided by HTML exist to organize and describe the content of web pages. Two of these HTML tags are `<em>` and `<strong>`. They are used to signal that the text within them should be "emphasized" or "strong." Later, when you begin to style websites you will decide how you want browsers to display content within `<em>` and `<strong>` tags. However, browsers have built-in style sheets that will generally style these tags in this manner:

* The `<em>` tag will generally render as italic emphasis.
* The `<strong>` will generally render as bold emphasis.

Take a look at each emphasis in action:
```
<p><strong>The Nile River</strong> is the <em>longest</em> river in the world, measuring over 6,850 kilometers long (approximately 4,260 miles).</p>
```
In this example, the `<strong>` and `<em>` tags are used to emphasize the text The Nile River (bolded) and longest (italics).

- [ ] Emphasize seven ages using the `<em>` tag.
- [ ] In the poem All the world's a stage, make the words men and women strong using the `<strong>` tag.

### Step 14: Line Breaks
The spacing between code in an HTML file doesn't affect the positioning of elements in the browser. If you are interested in modifying the spacing in the browser, you can use HTML's line break element: `<br />`. The line break element is a self-closing tag. You can use it anywhere within your HTML code and a line break will be shown in the browser.
```
<p>The Nile River is the longest river <br /> in the world, measuring over 6,850<br /> kilometers long (approximately 4,260 <br /> miles).</p>
```
The code in the example above will result in an output that looks like the following:
```
The Nile River is the longest river
in the world, measuring over 6,850
kilometers long (approximately 4,260
miles).
```
You may see line breaks written as `<br />` or `<br>`. Both are valid break tags.

Note: Line breaks are not the standard way of manipulating the position of HTML elements, but it's likely that you'll come across them every now and then.

- [ ] In the poem All the World’s a Stage, add a line break (`<br />`) after the comma (,) on the first line.

### Step 15: Unordered Lists
So far, all text has been in paragraph form. What if you want to display content in an easy-to-read list? In HTML, you can use an unordered list tag (`<ul>`) to create a list of items in no particular order. An unordered list outlines individual list items with a bullet point.

The `<ul>` element cannot hold raw text and cannot automatically format raw text into an unordered list of items. Individual list items must be added to the unordered list using the `<li>` tag. The `<li>` or list item tag is used to describe an item in a list.
```
<ul>
  <li>Limes</li>
  <li>Tortillas</li>
  <li>Chicken</li>
</ul>
```
In the example above, the list was created using the `<ul>` tag and all individual list items were added using `<li>` tags.

- [ ] Under the heading saying William Shakespeare create an unordered list. Add the following items to the list:
* Birth Date: 
* Death Date:
* Birth Location:
* Death Location:
Find out what year William Shakespeare was born and died and where and add this information to your unordered list.

### Step 16: Ordered Lists
Some lists, however, will require a bit more structure. HTML provides the ordered list for when you need the extra ordering that unordered lists don't provide. Ordered lists are like unordered lists, except that each list item is numbered. You can create the ordered list with the `<ol>` tag and then add individual list items to the list using `<li>` tags.
```
<ol>
  <li>Preheat the oven to 350 degrees.</li>
  <li>Mix whole wheat flour, baking soda, and salt.</li>
  <li>Cream the butter, sugar in separate bowl.</li>
  <li>Add eggs and vanilla extract to bowl.</li>
</ol>
```
- [ ] Under the heading the William Shakespeare heading and after the unordered list add the paragraph `<p>William Shakespeare's most popular work:</p>` followed by an ordered list with the top three most popular pieces of work by William Shakespeare (do the online research to find out which ones they are).

### Step 17: Images
All of the elements you've learned about so far (headings, paragraphs, lists, and spans) share one thing in common: they're composed entirely of text! What if you want to add content to your web page that isn't composed of text, like images?

The `<img>` tag allows you to add an image to a web page. This is another example of a self-closing tag.

```<img src="image-location.com" />```

The `<img>` tag has a required attribute called src. The src attribute must be set to the image's source, or the location of the image. In this case, the value of src must be the uniform resource locator (URL) of the image. A URL is the web address or local address where a file is stored. Note that the end of the `<img>` tag has a forward slash `/`. Self-closing tags may include or omit the final slash — both will render properly.

This example is our first mention of an attribute. However, the ids that we added to our div tags earlier are also attributes!

Attributes provide more information about an element's content. They live directly inside of the opening tag of an element. Attributes are made up of the following two parts:
* The name of the attribute
* The value of the attribute

- [ ] Right before the closing body tag add the following container:
```
<div id="media">
  <h2>Portrait</h2>
</div>
```
Add an image of William Shakespeare under the Portrait heading. Find an image online and use the URL that points directly to the image.

### Step 18: Image Alts
Part of being an exceptional web developer is making your site accessible to users of all backgrounds. Specifically, visually impaired users require more support from your web page so that they can experience the content on your page. HTML helps support visually impaired users with the alt attribute. The alt attribute is applied specifically to the `<img>` element. The value of alt should be a description of the image.
```
<img src="#" alt="A field of yellow sunflowers" />
```
The alt attribute also serves the following purposes:
* If an image fails to load on a web page, a user can mouse over the area originally intended for the image and read a brief description of the image. This is made possible by the description you provide in the alt attribute.
* Visually impaired users often browse the web with the aid of screen reading software. When you include the alt attribute, the screen reading software can read the image's description out loud to the visually impaired user.

Note: If the image on the web page is not one that conveys any meaningful information to a user (visually impaired or otherwise), the alt attribute should not be used.

- [ ] Add the alt attribute to the image. make sure the description actually describes the image.

### Step 19: Linking Out
We wouldn't be taking advantage of the full power of HTML (and the Internet), however, if we didn't link to other web pages. You can add links to a web page by adding an anchor element `<a>` and including the text of the link in between the opening and closing tags.
```
<a>This Is A Link To Wikipedia</a>
```
Wait a minute! Technically, the link in the example above is incomplete. How exactly is the link above supposed to work if there is no URL that will lead users to the actual Wikipedia page? The anchor element in the example above is incomplete without the href attribute. This attribute stands for hyperlink reference and is used to link to a file path, or the address to where a file is located (whether it is on your computer or another location).
```
<a href="https://www.wikipedia.org/">This Is A Link To Wikipedia</a>
```
In the example above, the href attribute has been set to the value of the URL https://www.wikipedia.org/. The example now shows the correct use of an anchor element.

- [ ] Below the image add a link to the wikipedia page about William Shakespeare (the link text should say William Shakespear).

### Step 20: Linking at Will
You've probably visited websites where not all links were made up of text. Maybe the links you clicked on were images, or some other form of content. So far, we've added links that were made up of only text, like the following:
```
<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank">Prickly Pear</a>
```
Text-only links, however, would significantly decrease your flexibility as a web developer!

Thankfully, HTML allows you to turn nearly any element into a link by wrapping that element with an anchor element. With this technique, it's possible to turn images into links by simply wrapping the `<img>` element with an `<a>` element.
```
<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank"><img src="#" alt="A red prickly pear fruit"/></a>
```
In the example above, an image of a prickly pear has been turned into a link by wrapping the outside of the `<img>` element with an `<a>` element.

- [ ] In index.html, transform the image on your page into a link (to the Wikipedia page about William Shakespeare) by wrapping the image element with an anchor element. Set the target attribute so that the link opens in a new window.

### Step 21: New Page
Have you ever clicked on a link and observed the resulting web page open in a new browser window? If so, you can thank the `<a>` element's target attribute. The target attribute specifies that a link should open in a new window. Why is it beneficial to open links in a new window?

It's possible that one or more links on your web page link to an entirely different website. In that case, you may want users to read the linked website, but hope that they return to your web page. This is exactly when the target attribute is useful!

For a link to open in a new window, the target attribute requires a value of `_blank`. The target attribute can be added directly to the opening tag of the anchor element, just like the href attribute.
```
<a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">The Brown Bear</a>
```
In the example above, setting the target attribute to `_blank` instructs the browser to open the relevant Wikipedia page in a new window.

Note: In this exercise, we've used the terminology "open in a new window." It's highly likely that you are using a modern browser that opens up websites in new tabs, rather than new windows. Before the advent of browsers with tabs, additional browser windows had to be opened to view more websites. The target attribute, when used in modern browsers, will open new websites in a new tab.

- [ ] In the text link that leads to the Wikipedia, add the target attribute and set it equal to `_blank`.

### Step 22: Relative Links
Thus far you have learned how to link to external web pages. Many sites also link to internal web pages like Home, About, and Contact.

Before we learn how to link between internal pages, let's establish where our files are stored. When making multi-page static websites, web developers often store HTML files in the root directory, or a main folder where all the files for the project are stored. As the size of the projects you create grows, you may use additional folders within the main project folder to organize your code.
```
about.html
contact.html
index.html
```
The example above shows three different files — `about.html`, `contact.html`, and `index.html` in one folder.

If the browser is currently displaying `index.html`, it knows that `about.html` and `contact.html` are in the same folder as `index.html`, also referred to as the current folder. Since the browser knows the current folder, other files in the folder can be linked using a relative path.

A relative path is a filename that shows the path to a local file (a file on the same website, such as `./index.html`) versus an absolute path (a full url, like `www.codecademy.com/learn/ruby` which is stored in a different folder). The `./` in `./index.html` tells the browser to look for the file in the current folder.
```
<a href="./contact.html">Contact</a>
```
In this example, the `<a>` tag is used with a relative path to link from the current HTML file to the `contact.html` file in the same folder. On the web page, Contact will appear as a link.

- [ ] Directly below the opening `<body>` tag, add an anchor tag that links to `index.html` with a relative path. The link should say William Shakespear. 
- [ ] Under the link to `index.html`, add an anchor tag that links to `about.html` using a relative path. The link should say About. Click the link to make sure it works!
- [ ] Create a new file called `about.html` and insert the following HTML code it it:
```
<!DOCTYPE html>
<html>
<head>
  <title>About</title>
</head>
<body>
  <nav>
    <a href="/">William Shakespear</a>
    <!-- web browsers respond to index.html and / the same way -->
    <a href="./about.html">About</a>
  </nav>

<h1>About</h1>
</body>
</html>
 ```
 
 ### Step 23: Same Page
At this point, we have all the content we want on our page. Since we have so much content, it doesn't all fit on the screen. How do we make it easier for a user to jump to different portions of our page? When users visit our site, we want them to be able to click a link and have the page automatically scroll to a specific section.

In order to link to a target on the same page, we must give the target an id, like this:

```
<p id="top"> This is the top of the page! </p>
<h1 id="bottom">This is the bottom! </h1>
```
In this example, the `<p>` element contains id of top and the `<h1>` element contains id of bottom. An id can be added to most elements on a webpage.

An id should be descriptive to make it easier to remember the purpose of a link. The target link is a string containing the # character and the target element's id.

```
<ol>
  <li><a href="#top">Top</a></li>
  <li><a href="#bottom">Bottom</a></li>
</ol>
```
In the example above, the links to `<p id="top">` and `<h1 id="bottom">` are embedded in an ordered list. These links appear in the browser as a numbered list of links. This is why we have been adding ids to our divs all along!

Under the `<h1>` element that says William Shakespear, create an unordered list with the following three list items:
* Top
* Bottom

- [ ] Wrap the text of each list item in the unordered list in an anchor element. Each anchor tag should link to the corresponding `<div>` on the page (The `<a>` element that contains the text "Introduction" links to #introduction).
