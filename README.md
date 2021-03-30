# Information about your Final Project Repository

## The following files and folders are part of the basic structure of our site and don't need to be edited by you:
__includes__: Folder with html pages for the extra goodies that came with this template, like social media icons and Google analytics. The only thing you’ll ever need to touch in here is the sidebar.html file, to create new links in the navigation bar. (See below for more instruction.)

__sass__: The CSS files for the extra material that comes along with the site. Really no need for you to touch this at all __except for the variables.scss file__. If you'd like to change the basic colors and fonts of your site, this is where you'd make site-wide changes.

__site__: This is where Jekyll keeps all the files created when it builds your site from your Markdown files and translated them to HTML. You don't ever need to touch anything in this folder. All of these files will constantly change as you develop your site.

__LICENSE, README, and script.js__ are all files that you shouldn’t touch. The license comes from the original writer of Jekyll Now (it’s totally open access), and the README file (which you're reading now) simply explains the repository to interested parties on GitHub. Finally, the script.js file contains the code for the sliding navigation sidebar.

## The following folders you are already familiar with from our course blog, so you should know how to add new files following exactly the same model we have for our digital tools assignments:

__people__: The folder where you’ll put your author bio pages. There’s a sample one in here to get you started. You already know how to customize one for yourself, because you did it for our course blog.

__posts__: The folder where you’ll put your posts, if you have them. You already know how to create new posts and load them into this folder. They’ll automatically show up on your homepage, if you decide to leave the format of your homepage as a blog feed. However, you may decide not to present your work in blog format, though you certainly can if you’d like.


## Files and folders that will be important for you as you build your site and want to tinker with its layout or its structure:

__congif.yml__: This file collects the basic info for your site. You'll simply fill it out once (and you should do this with your partner when you begin your project), and then you will likely never touch this file again.

__layouts__: This folder contains the basic HTML that serves as the template for the different categories of pages on your site. Jekyll takes the Markdown content of your individual posts or pages and then styles them according to the HTML templates laid out in this folder. That's why these files are all written in HTML. If you’d like to play around with the basic layout of your site, you’ll need to edit these pages using HTML. You certainly don’t have to--these pages will work fine just as they are--but if you’d like to, there are basic HTML tutorials available for free on the web, like [this one](https://www.codecademy.com/learn/learn-html) from CodeAcademy which is very good. It includes the following files:

- __author.html__: The template for contributor bio pages that will automatically search and update a list of posts you’ve created. You won’t need to tinker with this.
- __default.html__: Contains the layout you want to appear on _every single page of your website_: header and footer, nav, and some meta-data script. If you want to fiddle with the layout of your masthead or footer, you’d do it in this file.
- __page.hmtl__: The basic layout for any .md file designated as “page” in the header. You shouldn’t need to tinker with this, but who knows, you might!
- __post.html__: The basic layout for any .md file designated as “post” in the header. Not much here to fiddle with, but you may want to.

__style.scss__: This is the file that contains the CSS (Cascading Style Sheets) code to change how your site looks (fonts, colors, positioning of text blocks and images). If you want to make design layout changes to your site, this is where you do it. However, this isn’t a web design course, and I’m not grading you on the aesthetics of your site, so don't feel obligated. We will go over a couple of places where you can easily make basic changes to colors and fonts, but there is no expectation that you will go beyond that. If you'd like to learn more about CSS [this free lesson](https://www.codecademy.com/learn/learn-css) from CodeAcademy is also very good.

## The following files are __pages__ and they just float free in the "root" directory of your site, rather than living in a designated folder like __posts__ do:
__404.md__: A custom 404 page for your site! If a link is broken, this is what will pop up. You can edit the file with whatever you’d like.

__index.md__: This is the homepage of your site. Right now it’s set up as a feed of blog posts. You can keep it that way, or you can add information about your project as a landing page. Or you can remove the blog feed all together!

These are the only two __pages__ that are mandatory for your site. You can delete the __about.md__ file if you don’t want to have an “About” page for your project in addition to your home page, but it's probably a good idea to have one. You can also create as many new pages for your site as you’d like and customize them as you see fit. See directions below!


## How to Create New Pages for your Final Project Site
Create a new .md file in your repository--the root directory of your site--and, in the header info at the top, set it to:
```
---
layout: page
title: Your Title Here
---
```
Unlike __posts__, pages don’t automatically show up on your site. You need to create links within your site so that users can access them. You may want some of these links to exist in the Navigation menu on the sidebar. If so, you’ll need to edit the navigation links in the __sidebar.html__ file. You may just want to link to new pages through other pages, and that's also just fine.

Maybe instead of an “About” page, you want a page called “History” in your navigation menu. So here’s how you make one:

1. Create a new .md file in your repository (not within a folder, just in the repository) called __history.md__.
2. Use the header settings above, and write the page in Markdown as you would any blog post. Save your changes.
3. Open the __includes__ folder, and then open __sidebar.html__. This file has the template for the navigation bar with this HTML within it.

```
<nav class=”sidebar-nav”>
<h2>
  <a class=”sidebar-nav-item” href="{{ site.baseurl }}/">HOME</a>
  <a class=”sidebar-nav-item” href="{{ site.baseurl }}/about">ABOUT</a>
<h2>
</nav>
```

Just change it to:
```
<nav class=”sidebar-nav”>
<h2>
  <a class=”sidebar-nav-item” href="{{ site.baseurl }}/">HOME</a>
  <a class=”sidebar-nav-item” href="{{ site.baseurl }}/history">HISTORY</a>
<h2>
</nav>
```
Note that you've changed both the link itself from `{{ site.baseurl }}/about` to `{{ site.baseurl }}/history` *and* the text that appears in the sidebar, from `ABOUT` to `HISTORY`.

In both HTML and in Markdown, you can use this exact formula anytime you want to add a link to other pages *held within your site* (this includes links to files of images or PDFS that you might want to save in a folder in your site too):

HTML: `<a href=”{{ site.baseurl }}/filename”>Link Text</a>`

Markdown: `[Link Text]({{ site.baseurl }}/filename)`

If you’re trying to link to, say, an image file in a folder, or a PDF file in a folder, you would follow the same format, just including the folder extension before the file:

For a link to a PDF:

HTML: `<a href=”{{ site.baseurl }}/folder/filename”>Link Text</a>`

Markdown: `[Link Text]({{ site.baseurl }}/folder/filename)`

For a link to an image file stored in your repository:

HTML:  `<img src=”{{ site.baseurl }}/folder/filename” />`

Markdown: `![Alt Text]({{ site.baseurl }}/folder/filename)`


##Finally, all of the Markdown rules apply to your final project repository too.
So be sure to consult the rules listed below!

### Rule #1: All of the Markdown syntax you learned from the Getting Started with Markdown lesson applies!
You should follow this basic syntax when writing your Digital Tools Assignments.

### Rule #2: Post Titles
- The title of your post in your post’s header will display on our blog; no need to use that same title in the post itself. You may want to open with a subtitle, and that’s fine (like, for example, “Introduction” or something), but you don’t need to repeat your post’s main title in the body of your post. It looks redundant on the blog!
- No colons in the post titles you create in your header. Colons confuse the Jekyll convertor and it doesn’t know what to do with your post. Just use a dash instead.

Instead of this:
```
---
layout: post
author: Melissa Reynolds
excerpt_separator: <!--more-->
title: Academics Cannot Write Titles Without Colons: A Study
---
```

Better to write this:
```
---
layout: post
author: Melissa Reynolds
excerpt_separator: <!--more-->
title: Academics Can Write Titles Without Colons - But Only in Markdown
---
```

### Rule #3: Use ## or smaller for your subheadings and subtitles within your posts, not #.
This rule is strictly aesthetic. The CSS style sheet for our site renders your post titles as `<h2>` in HTML, which means that any subheadings in `<h1>` look disproportionate. Again, this is an aesthetic rule just for our course blog, not one that applies to any other places you might use Markdown!

### Rule #3: Embedding, aligning, and resizing an image.
I’ve added some CSS to our style sheet to make this possible on our  course website. The basic CSS that comes in Jekyll-ready templates doesn’t include the ability to resize images or align them unless you insert HTML or directly load the file into an “images” folder in your repository. Here’s what you do:

Follow the usual syntax for embedding an image using Markdown, just like always, but add the following extra stuff at the end:`![Alt text](https://linktoimage.jpg){:width=”450px” .center-image}`

You can of course change the pixel value to whatever you’d like, but be sure it’s in quotation marks. You can also use the following commands to align your image to the left or right and float your text around your image:

For left aligned: `![Alt text](https://linktoimage.jpg){:width=”450px” .left-image}`

For right aligned: `![Alt text](https://linktoimage.jpg){:width=”450px” .right-image}`

Note that when your image is center aligned, your text will appear underneath the image and will not float around it. When you use right or left aligned, the image will be nestled within a text block.

Now that we know how to do this, best practices for embedding images within your post would be to always use a URL rather than a file.
If you must download a photo to use it, host it on your personal GitHub account in a public repository, but not the one you forked from HUM-331-Princeton (because then when you send a pull request it will merge into our class repository). Once the image is hosted publicly on GitHub, you can simply right click the image and copy the link address.

### Rule #4: Setting an “excerpt” for your post to be displayed on our home page.
In its default mode, Jekyll automatically selects the first paragraph of your post as an “excerpt” that will be displayed on the home page of our blog, followed by a link to READ MORE.
Sometimes, though, it doesn’t work like it’s supposed to, or maybe you want to include a bit more in the preview that readers see on our course home page, like an image or a longer section of text.
If so, you can simple add this to your posts header material:
```
---
layout: post
Author: Your Name
excerpt_separator: <!--more-->
Title: Your Post Title
---
```
Now, in the body of your post, wherever you want the post to break on the home page and link to __READ MORE__, you insert that symbol exactly: `<!--more-->`

### Rule #5: Be aware of `|` cropping up in citations
Many of you included a “Works Cited” section in your last Digital Tools Assignment, which is great. But, by default, it’s pretty common for a website title to look like this, `1756: Nassau Hall | Princetoniana Museum,` with a vertical line separating the page name from the site name. Unfortunately, this vertical line is the same symbol used in Markdown to indicate that you want to display information in a table format. You’ll end up with text that has weird spacing in the middle of the line, and it’ll look funky in your post. Best to convert `|` into “–” to fix this problem.


## Credits
- [Jekyll Now](https://github.com/barryclark/jekyll-now) - Thanks to Barry Clark for the basic template with infinite customization possibilities.
- [Jekyll](https://github.com/jekyll/jekyll) - Thanks to its creators, contributors and maintainers.
- [Lanyon](https://github.com/poole/lanyon) by MDO - Thanks to its creators for the slide-out navigation sidebar.
- [SVG icons](https://github.com/neilorangepeel/Free-Social-Icons)
- [Solarized Light Pygments](https://gist.github.com/edwardhotchkiss/2005058)
