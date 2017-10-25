---
title: Href
---

## Href

This is a stub. [Help our community expand it](https://github.com/freeCodeCamp/guide-articles/tree/master/articles/HTML/Attributes/Href/index.md).

[This quick style guide will help ensure your pull request gets accepted](https://github.com/freeCodeCamp/guide-articles/blob/master/README.md).

The href defines the document to which the link leads. This may be a web page in the same directory, a page somewhere else on the same server, a location within the current page, or a web page—or any another kind of document—stored on another server.

The example shows a link between two documents in the same directory, but if the cake list document was in a directory that’s one level higher than the referencing document, the syntax would be as follows:

<a href="../cakes.html">lovely range of cakes</a>
Here, ../ equates to the instruction, “move up one directory in the hierarchy.”

You can also reference a document relative to the web site’s root (the file or folder after the domain name):

<a href="/cakes.html">lovely range of cakes</a> 
This link basically instructs the browser to “link to the document cakes.html that can be found in www.mydomain.com/.” This is a very handy way of referencing documents, as you could move the document containing the link to any location on the file system without breaking the link.

If you’re linking to a document (of whatever type) that’s held on another server, you’d express the href using a complete URI, like so:

<a href="http://www.cakebrothers.com/cakes.html">lovely range of cakes</a>
In a link to another section within the same page, the destination is identified in the href attribute by a hash symbol combined with the id attribute of the destination. This notation is known as a fragment identifier, and is shown below:

<!-- Here is the link -->
<p>You can check the facts by reading the
  <a href="#refs">references at the end of this article</a></p>
⋮
<!-- Here is the link's destination -->
<h3><a id="refs" href="#refs">References</a></h3> 
Note these points from the example above:

The href attribute is repeated in the second a element. This isn’t a mistake—it’s there because without it, Internet Explorer users who navigate to the destination would find that, although the document had moved to the correct position on the screen, the focus will not have shifted. If the user were to tab to the next link, the focus would move to the link immediately after the link the user had selected further up the page, rather than the next link after the point in the page at which the references are included.
It’s possible to simply apply an id attribute to another element—for example, <h3 id="refs">References</h3>—and some browsers will allow you to activate a link and jump to that point. However, not all browsers allow this, the notable case being Internet Explorer. That’s why we need the seemingly superfluous second a element as an anchor, which is wrapped around the text inside the h3. The syntax for this simplified (but not IE-friendly) markup is shown below:

<p>You can check the facts by reading the
  <a href="#refs">references at the end of this article</a></p>
⋮
<h3 id="refs">References</h3> 
In your own work, you may spot examples that include both a name and id inside the anchor a element. This approach is designed to ensure that the link works in older browsers which may not allow the user to jump from one part of a document to another if the name attribute isn’t present. However, the last of the common browsers that weren’t able to link to a section of a page in this way was Netscape 4, which, thankfully, is now almost completely obsolete. Also, note that in HTML 5 the name attribute has been removed, so it’s a good idea to break the habit of using name.

In addition to links to documents (such as web pages or other document types), the href attribute may specify a different protocol, including:

ftp typed as <a href="ftp://someftpserver.com/">Browse the FTP server</a>, which will open a connection to an FTP server
mailto typed as <a href="mailto:mrwhatever@somedomain.com">Email me!</a>, which will trigger an email client to open and create a new message whose To address matches whatever appears after the mailto: protocol (in this case, an email to mrwhatever@somedomain.com)

#### More Information:
<!-- Please add any articles you think might be helpful to read before writing the article -->


