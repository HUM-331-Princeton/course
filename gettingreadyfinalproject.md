---
layout: page
title: Getting Ready for our Final Projects
---

The first thing we’re going to do is download and install **Atom**, my favorite text editor for working directly with GitHub. It’s got Git built into it and will sync easily with your GitHub account.

## To be done before class on Wednesday, March 31:

1. Go to [atom.io](https://atom.io). Click Download.
2. Once Atom is downloaded, double click to unzip the file. If you’re on a Mac, you’ll need to open your Downloads folder and move Atom into your Applications folder.
3. Open the application by double clicking it.
4. If you don’t already have developer command line tools installed on your computer, you may see a dialogue box pop up that says: “The ‘git’ command requires the command line developer tools. Would you like to install the tools now?”
5. Click Install and agree to the licensing terms to Install XCode. Click Install, not Get XCode, if that’s an option you see.
6. When you open Atom, you’ll see a menu at the bottom right. Click GitHub. You’ll be asked to go to github.com to sign in and get a code to link Atom with your account.

Great, you’ve got Atom! We’ll work in Atom in class on Wednesday, so you’re all set for now.

## To work through in class on Wednesday, March 31:

Now we’re going to head over to GitHub, to the [HUM-331-Princeton repository](https:://github.com/HUM-331-Princeton). You’ll see a new repository in the organization: **HUM-331-Princeton/final-project-template**.

I created this template for you all to use for your final project, but it’s really just a copy of a pretty popular (and really user-friendly) Jekyll template known as Jekyll Now that I’ve customized with a sidebar navigation and a contributors template. It is a very basic website that you can customize with extra HTML or CSS if you’d like, but it also functions really simply right out of the gate.

1. Open the repository final-project-template.
2. If you’re working with a classmate as a pair for your final project, *just one of you* should click Use this template to create a new repository based on exactly these files.
3. Be sure to select HUM-331-Princeton as the owner of the repository, not your personal account.
4. Decide what you want to call the repository, and keep in mind that this will end up in the URL for your site, so pick something that conveys a bit about your project but keep it short—like no more than three words at most.
5. Add a description that says something about the site and your project, and select Public.
6. Navigate to **Pages** in the sidebar menu, and select **main** in the drop down menu. Keep the source as **/(root)** and click Save.
7. In the left-hand menu, navigate to **Manage Access**. Whichever one of you created the new repository, invite the other member of your group by typing their GitHub account name into the box. Be sure to select **Admin** as that person’s privileges in the repository.
8. In the left-hand menu, navigate to **Notifications** and enter your email addresses.
9. Give it a few seconds (or maybe a minute or two) and direct your browser to HUM-331-Princeton.github.io/whatever-you-named-your-repository
You should see a bare bones demo site, ready for you to customize!

Ok, you’ve created a site, that’s awesome!

**Now it’s time to put the files on your local computer so you can work on your final project without constantly clicking around GitHub. We’re going back to Atom.**

1. Open Atom and click the GitHub menu at the bottom right.
2. You should see a menu option to “Clone an existing GitHub repository…”
3. Click that option, and you’ll see a box pop up with a space for you to paste in the URL of your new repository.
4. Go back to GitHub.com and copy the URL for your new repository. This is the GitHub URL not the URL for your new site. So it should be:
github.com/HUM-331-Princeton/whatever-you-named-your-project
5. Now paste that address into the box and pay attention to where it’s getting saved in your computer. Atom will automatically create a file on your computer called github, but it won’t be in your Documents or Desktop unless you specify that location. If I wanted the folder to be in Documents, I would need to edit the path for the repository files to: Users/melissareynolds/Documents/github/whatever-you-named-your-site.
6. Click Clone and you should see all the files from your new repository appear!
7. Edit your **config.yml** file with your site title, description, and updated url. **This will only be done once.**
8. Save those changes. Toggle the **git** menu on the bottom right. You'll see the file **config.yml** in the **Unstaged Changes** list.
9. Click **Stage All** and see the **config.yml** file move down to the **Staged Changes** box. Type in a **commit message** and click **Commit to main**.
10. At the bottom right menu, click **push**. You've now sent your changes to the remote repository!
11. From now on you'll work in your own branch, rather than in the **main** branch so that you and your partner can make changes without cancelling each other's work out. Click **main** and click **New branch**.
12. Type in the name of your branch as **firstname--MM-DD** and then click **New Branch** again. You've got your own branch now and you can get to work!
