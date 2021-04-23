---
layout: page
title: Turning texts into data with XML and TEI
---

As you know from class, XML is a metalanguage (a language used to describe or markup another language) used in order to process and store texts in digital format. Markup languages are valuable as means of helping digital archivists and instructional technologists do two things: first, markup creates a rich data set from the text in question which can then be converted into a number of formats; second, markup encodes how a particular text should be presented on a webpage, digital publication, data set, etc. Markup languages thus guide our interpretations of those texts. Considerations like spacing, bolding, and headings are all aspects of the markup process—which is often also referred to as “encoding.” Marking up a document in XML is a matter of directing a person as to how the manuscript’s content should be presented and interpreted.

For this assignment, you may use a recipe from the Kislak Center’s online archive on [From the Page](https://fromthepage.com/upenn/kislak-center-recipe-books/arts-and-sciences-manuscript-chemistry) in order to create your own TEI markup, or you may choose a text related to your final project to mark up.

## Step 1: Document Analysis:

1. What about the format of the document would you like to make legible in a digital representation? Does your chosen document have a front and back? Paragraphs or lines of poetry? Dialogue? Lists? Images?
2. What are the elements (content) of the text that you'd like to make legible as data? Are there different languages? Bold text? Emphasized text? Place names or people's names? You can refer to the glossary of official TEI elements [here](https://tei-c.org/release/doc/tei-p5-doc/en/html/REF-ELEMENTS.html), or you can review the basic TEI tags in the [Basic Tagging tutorial](https://www.wwp.northeastern.edu/outreach/seminars/_current/presentations/basic_encoding/basic_encoding_tutorial_00.xhtml) from the Women Writer's Project.
3. Write your TEI schema so that you have a root and elements nested within that root, i.e. `<div>`, `<head>`, `<text>`, `<image>`, `<persName>`, etc.
Strive for at least 5 different elements or attributes that capture the basic structure and content of the text.

## TEI Markup in Markdown:

1. In your text editor, create an .md file to compose your blog post with TEI mark-up. Remember that you'll want your mark-up to show up as code on our website, which means you'll need to use the appropriate Markdown syntax to set off your code from the rest of your blog post. (Hint: bracket your markup code with triple ticks at the start and at the end. You can always refer back to the [Getting Started with Markdown](https://programminghistorian.org/en/lessons/getting-started-with-markdown) lesson you completed at the start of the semester.)
2. Encode the body of the text.
3. Copy and paste your TEI into [Code Beautify](https://codebeautify.org/xmlvalidator) if you'd like to check for open tags and broken elements.
4
## Explain yourself:

Now in the same .md file, write a 4-5 paragraph blog post explaining how you developed your TEI hierarchy:

- What aspects of the document do I want to tag for a researcher?
- How can I categorize this document? What markup codes will be useful?
- What textual structure seems appropriate? Consider the hierarchy of your tags.
- What questions about markup emerged throughout the process?

## Submission:

You'll upload your post to a new branch in our class repository just like you did last time. Name your new branch **yourname-XML** and upload your post into the **_posts** folder. Finish by submitting a **pull request** to the **_master** branch of our class repository.

## An example of the TEI markup used in the Making and Knowing digital critical edition that we looked at in class:

__Sample #1: A Markup of a Recipe featured in Secrets of Craft and Nature:__

```xml
<page>040r</page>
<image>http://gallica.bnf.fr/ark:/12148/btv1b10500001g/f85.image</image>

<div>

<id>p040r_3</id>

<head><m>Vinegar</m></head>

<ab>One takes for granted that <del><fr>jec</fr></del> heat red-hot the <m>mineral salt</m> that looks like <m>marble</m> & that is called in <pl>Catalonia</pl> & at the border of <pl>Spain</pl> <m><pl>Cardona</pl> salt</m>, & throwing it <del>in the</del> red hot or quite hot in <m>wine</m>, it turns it into very good <m>vinegar</m>. Some make it with <m>water</m> poured on pomace soured after being pressed by <pro>grape pickers</pro>, but it will not keep & spoils in heat & thunder storms.</ab>

</div>
```
