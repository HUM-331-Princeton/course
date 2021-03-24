# Information about your Final Project Repository

__includes__: Folder with html pages for the extra goodies that came with this template, like social media icons and Google analytics. The only thing you’ll ever need to touch in here is the sidebar.html file, to create new links in the navigation bar. (See below for more instruction.)

__layouts__: This folder contains the basic HTML that serves as the template for the different categories of pages on your site. Jekyll takes the Markdown content of your individual posts or pages and thenThese files are all written in HTML, and if you’d like to change the order of information on your site, or play around with its basic layout, you’ll need to edit these pages using HTML. You certainly don’t have to--these pages will work fine just as they are--but if you’d like to, there are basic HTML tutorials available for free on the web, like this one from CodeAcademy, and this one from Mozilla.
author.html: The template for contributor bio pages that will automatically search and update a list of posts you’ve created. You won’t need to tinker with this.
default.html: Contains the layout you want to appear on every page: header and footer, nav, and some meta-data script. If you want to fiddle with your masthead or footer, you’ll do it in this file.
page.hmtl: The basic layout for any .md file labeled as “page” in the header. You shouldn’t need to tinker with this, but who knows, you might!
post.html: The basic layout for any .md file labeled as “page” in the header. Not much here to fiddle with, but you may want to.

__people__: The folder where you’ll put your author bio pages. There’s a sample one in here to get you started. You already know how to customize one for yourself, because you did it for our course blog.

__posts__: The folder where you’ll put your posts, if you have them. You already know how to create new posts and load them into this folder. They’ll automatically show up on your homepage, if you decide to leave the format of your homepage as a blog feed. However, you may decide not to present your work in blog format, though you certainly can if you’d like. 

__sass__: The CSS files for the extra material that comes along with the site. Really no need for you to touch this at all.

__congif.yml__: The basic info for your site that you’ll simply fill out like a form. Once you add your site info the first time (and you should do this with your partner when you begin your project), you will likely never touch this file again.

__CNAME, LICENSE, README, and script.js__ are all files that you shouldn’t touch. The CNAME file would be used if you had a custom domain name instead of one at “github.io,” the license comes from the original writer of Jekyll Now (it’s totally open access), and the README file (which you're reading now) simply explains the repository. Finally, the script.js file contains the code for the sliding navigation sidebar.

__style.scss__ is the file that contains the CSS code to change how your site looks (fonts, colors, positioning of text blocks and images). This isn’t a web design course, and I’m not grading you on the aesthetics of your site, but CSS is fairly easy to intuit and there are several tutorials on the web to help you learn the basics, like this one from CodeAcademy and this one from Mozilla. If you want to make design layout changes to your site, this is where you do it. 

The following files are all designated as __pages__:
__404.md__: A custom 404 page for your site! If a link is broken, this is what will pop up. You can edit the file with whatever you’d like.
__index.md__: This is the homepage of your site. Right now it’s set up as a feed of blog posts. You can keep it that way, or you can delete what’s in there and add information about your project as a landing page. Or, you can do both, as I have for our class blog. Up to you!

These are the only two pages that are mandatory for your site. You can delete the __about.md__ file if you don’t want to have an “About” page for your project. You can also create as many pages for your site as you’d like and customize them as you see fit. See directions below!




## How to Create New Pages for your Final Project Site
Create a new .md file in your repository (not in a folder) and, in the header info at the top, set it to:
```
---
layout: page
title: Your Title Here
--- 
```
But—-and this is important—-your pages won’t automatically show up on your site like posts do. You need to create links within your site so that users can access them. You may want some of these links to exist in the Navigation menu at the top of your site. If so, you’ll need to edit the navigation links in the __sidebar.html__ file.

Maybe instead of an “About” page, you want a page called “History” with a discussion of the contextual background of your source. So here’s how you make one:
Create a new .md file in your repository (not within a folder, just in the repository) called __history.md__.
Use the header settings above, and write the page in Markdown as you would any blog post. Save your changes.
Open the __includes__ folder, and then open __sidebar.html__. This file has the template for the navigation bar with this HTML within it.

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

So let’s talk about what this syntax means: in both HTML and in Markdown, you can use this formula for coding in links to other pages within your site (this includes links to files of images saved in your site too):
		
HTML: `<a href=”{{ site.baseurl }}/filename”>Link Text</a>`

Markdown: `[Link Text]({{ site.baseurl }}/filename)`
		
If you’re trying to link to, say, an image file in a folder, or a PDF file in a folder, you would follow the same format, just including the folder extension before the file:

For a link to a PDF:

HTML: `<a href=”{{ site.baseurl }}/folder/filename”>Link Text</a>`

Markdown: `[Link Text]({{ site.baseurl }}/folder/filename)`

For a link to an image file stored in your repository:

HTML:  `<img src=”{{ site.baseurl }}/folder/filename” />`

Markdown: `![Alt Text]({{ site.baseurl }}/folder/filename)`


Finally, all of the Markdown rules apply to your final project repository too. 
So be sure to consult the rules listed below!

# Markdown Rules for Composing Posts and Pages

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
- [Lanyon](https://github.com/poole/lanyon) by MDO - Thanks to its creators for the slideable navigation sidebar.
- [SVG icons](https://github.com/neilorangepeel/Free-Social-Icons)
- [Solarized Light Pygments](https://gist.github.com/edwardhotchkiss/2005058) 


