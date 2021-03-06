---
layout: page
title: Getting Started with Markdown
---

By now you've created a [GitHub](https://github.com) account, practiced opening a repository, making changes to a file, making a pull request, and merging branches with GitHub's [Hello World](https://guides.github.com/activities/hello-world/) tutorial. You've followed the [Markdown lesson](https://programminghistorian.org/en/lessons/getting-started-with-markdown) on the Programming Historian, so you know how to style your text files with Markdown syntax. We've practiced authoring Markdown files in class, but now it's time to do it on your own and create content for our course blog. You'll be following these same steps to create and submit the rest of your Digital Tools assignments, so it's very important for you to get the hang of these basic steps now.

## Step 1: Think about downloading a text editor

All of your digital assignments this semester will be authored in Markdown, which means you can't use Google Docs or Microsoft word to create them. As you know, you can always create Markdown files (.md) directly in GitHub, but if you'd like to be able to complete your assignments offline or save your work on your own machine, you may prefer to use a text editing program to write and save your .md files. If you've done some programming/coding before, you likely already have a favorite text editor, and you should keep using it. If not, I really like [Atom](https://atom.io) because it works on all operating systems and it's an all-in-one program (you can connect it directly to your GitHub account), but other good options are BBEdit (Mac) and Notepad (Windows). Ok, you've thought about getting a text editor and now you're ready to...

## Step 2: Take a look at an existing post

Open the class repository that you've forked into your personal GitHub account. Find the **_posts** folder and open it. You'll see a single file in there titled **2020-11-15-Welcome to HUM 331.md**. This is the Markdown file for the blog post that appears on the homepage of our course website. Note the file naming conventions. All of the blog posts created for our site must be named in the same way: **yyyy-mm-dd-your title.md**.

Click the name of the file to open it, and then click on the pencil icon in the upper right to edit the file. You should now see the post written in Markdown with a header at the top that looks like this:

 ```
 ---
 layout: post
 author: Melissa Reynolds
 title: Welcome to HUM 331
 ---
 ```

Note the formatting of this file. The heading at the top is very important. Every post that you write for our course site must include this same header, though of course you'll change whatever comes after the "title" field to your chosen title. Without the header, Jekyll doesn't know to turn your Markdown file into a webpage.

## Step 5: Write a new post in Markdown

Either click **Add File** and then **Create New File** within your forked GitHub repository, or open your text editor of choice and create a new Markdown file with the appropriate naming conventions: **yyyy-mm-dd-your title.md**. ALL posts you create for this course blog must follow these exact naming conventions.

Now complete your assignment: write a 2???3 paragraph post describing sources and methods you'd ideally like to work with for your final project. Write carefully and with precision! You should think of this as equivalent to a 1 page reflection paper. You can be speculative at this point--I won't hold you to what you write here--but you must include the following, rendered correctly in Markdown syntax:

- Include at least one hyperlink to the digital source you'd like to use
- Include at least one embedded image in your blog post
- Use headings to distinguish between sections of your blog post
- Incorporate one bulleted list

As you write, think about the following questions:

1. What are your chosen sources and where are they located?
2. What would you like your readers/viewers to know about these sources?
3. What kinds of digital tools might you be interested in using to analyze these sources?
4. What are some of the challenges you foresee in working with your chosen sources?

## Step 6: Commit your post

(Note: the following instructions are for those of you brand new to GitHub, who don't use GitHub desktop or a text editor with built-in Git integration like Atom. This is the *most basic* way to add a file to your repository, but if you already know how to push changes and commit via those other platforms, go right ahead.)

If you've written your post directly in GitHub, you now just need to click the green **Commit** button to save the post to your repository. If you've drafted your post on your computer in a text editor, simply click **Add File** and then **Upload Files** and either drag and drop or select your Markdown file to upload. You can then **Commit** that file to your repository as you would one authored directly in GitHub.

## Step 7: Create a pull request

You've written your post and committed it to your **_posts** folder in your personal repository. In the menu at the top of your repository, click **Pull requests**. Click the green button **New pull request**. You'll now see a gray box at the top that shows you the base repository you'll be sending your changes to (HUM-331-Princeton/HUM-331-Princeton.github.io), and the head repository, which is yours.

Name your pull request **Markdown Post Assignment** and then click **Create pull request**.

Ok, that's it! You've written a blog post in Markdown and followed the standard GitHub workflow to send it to our class site. Pat yourself on the back, and know that you'll do it all over again for the next three assignments.

After I grade your post, I'll contact each of you individually before merging your pull request into our course repository to be sure you're comfortable sharing your work on our course blog.
