# {{ book.sections.about_drupal.the_stack }}

The single most-important factor a new Developer, Administrator, etc. should understand is the "Stack".

Unfortunately, there are *many* different 'Stacks' to learn about.

### LAMP Stack - \(Linux, Apache, MySQL, PHP\)
The LAMP stack is the traditional installation used for your first Drupal build, no matter the role. With the exception of the last one. Drupal has always been, and probably will always be, developed in PHP. Converting to other languages such as Python, JAVA, Ruby on Rails each have their own advantages, but there would be **no** upgrade path \(more on upgrade paths later\) available for current servers and current projects. This would also nullify the knowledge-base of current Developers and, most likely, cause the entire Drupal Community to fall apart. Thus, Drupal has been, and will most likely always be, a PHP software.

#### Other possible Server-Stacks used for a Drupal installation might be:
 + \(Unbuntu, Nginx, NoSQL, PHP\)
 + \(Raspbian, Apache, MySQL, PHP\)
 + The MAMP Stack - On Mac: \(MAC OSX, Apache, MySQL, PHP\)
 + The WAMP Stack - On Windows: \(Windows, Apache, MySQL, PHP\)
  - See the (pending) Linux page of the book for a high-level review of different Linux platforms and commands for Drupal.

### [The (Drupal) Technology Stack](https://www.drupal.org/node/176052 "Technology Stack")
The Drupal Technology Stack is merely the LAMP Stack expanded to include the Drupal framework.
<pre><code>- Linux
- Apache
- MySQL
- PHP
- Drupal</pre></code>

However, these are not the only stacks to know!

### The Browser Stack

The Browser Stack, known by dozens of other names, is a combination of more parts than we this book can fully address, but we will certainly make a good try of it!

To understand **your** web-browser, we must first dig in to he history of web-browsers in general. To do this, we look to one of the authorities on all things **"The Internet"**: the World Wide Web Consortium [WC3](https://www.w3.org/ "The World Wide Web Consortium (W3C)").

 The [WC3](https://www.w3.org/ "The World Wide Web Consortium (W3C)") has this explanation for how your web-browser works:
 > An HTML or XML document can be represented as a tree. Each document has one root or root node, which contains children or nodes, and which themselves can have children. Generally speaking, the leaves contain the text of document.
 > via [Philippe Le Hégaret, circa 2002](https://www.w3.org/2002/07/26-dom-article.html "Philippe Le Hégaret, circa 2002")

The article, truthfully, is positively **ancient** from a technical standpoint. 2002 is practically the Stone Age when you consider the progress society has made in recent years in such technologies as Virtual Reality (VR), Big Data Analytics & Augmentented reality.

In a more technical, and up to date, definition, [WC3](https://www.w3.org/ "The World Wide Web Consortium (W3C)") defines the Document Object Model as:
> The Document Object Model is a platform- and language-neutral interface that will allow programs and scripts to dynamically access and update the content, structure and style of documents. The document can be further processed and the results of that processing can be incorporated back into the presented page.
> via [Philippe Le Hégaret, circa January 19, 2005](https://www.w3.org/DOM/ "Philippe Le Hégaret, circa 2005")

So what are the key points herein?

*The DOM is platform and language neutral* - This means, theoretically, development can occur on any operating system, using any language. In theory, a Developer could conceivably build an entire website in COBAL.... but who would **want** to?
