---
layout: page
title: ""
---

## System set-up

1. Make a github account.
2. send it to Dika who will add you to the repo.

Download:
3. PyCharm (community edition)
4. Github desktop

5. Log into Github Desktop with your Github account. 
6. Go to the website repo on github.com and click on the large button that says 'clone'. 
7. Choose 'open with github desktop'. 
8. Choose where you want to save the repo locally. 
9. Press accept.

Once you see it in your GitHub desktop, click on 'open in Pycharm' in the middle of the screen. This
will open your repo in Pycharm and you'll be able to update/amend the code.

To see the local version of your website so you can see how your changes look, you'll need to host it locally. To do that:
10. Click on 'Terminal' at the bottom of your Pycharm screen.
11. If this is the first time youre doing this, you will need to type in 'bundle install' and enter. This will install the packages
you need to locally host. Skip this step if youve already done this.If this throws errors, contact Dika. You will only have to do this once.
12. Type 'bundle exec jekyll serve' to render the page locally. 
13. Click on the link you see in your terminal now (looks something like 127.0.0.0:localhost). This will open the local version
of the website in your browser. You can start applying changes now. Whenever you change something in the pycharm, refresh the page on your
browser to see how it looks.


## Updating the website

14. Before you start changing your code, go back to Github.com onto the repo and click on 'issues'.
15. Select the issue you want to work on or press 'new issue' and write in what you will do (e.g. 'update about page'). 
16. Press submit new issue. This will publish the issue to the repo so everyone knows the changes youre about to apply. 
17. On the right-hand side press on 'create branch'. Choose 'open branch with github desktop. 
18. Press the 'create branch' button. This will be the branch you will work on so your changes are not applied until they are finished.
19. Apply changes on your Pycharm (see instructions below). Check them using 'bundle exec jekyll serve'.
20. When youre happy with the changes, go to your GitHub desktop.
21. The changes youre about to push are on the left-hand side of the screen. Untick everything that starts with .idea/ or _site/ - those
are local files we dont need on the repo. Ensure the items which are ticked are only the ones you just worked on.
22. At the bottom of the left-hand side, type a summary of the changes (e.g. updated about page with contact details). 
23. Click on 'commit to [BRANCH NAME]'.
24. Press 'push origin' on the top line of GitHub desktop. This will send your changes to the GitHub repository.
25. Go to Github.com and go to 'code' tab. You'll see that your commits have been received because there will be a button at the top of the
code with a blue button that says 'Compare & Pull Request'. Click on it. 
26. Then click on 'Create pull request'. 
27. Someone else can then approve your changes.

This method ensures no work is ever lost or any changes applied in error. This is best practice.


## Website layout

This is a simple website. All you can see on the landing page is defined in:
``_layouts/home.html``

The items in the menu are defined in
``_data/menu.yml``

The about.md page, join.md page, work in progress.md and workshops.md are located at base level.
Apply changes in html language to those pages. Syntax examples are in Syntax_Examples.md for your convenience 
and include things such as how to add a url, how to indent your writing, how to add an image. Copy and paste from this 
file.

If you wish to add a page, copy and paste one of the .md pages (e.g join.md) and name it something descriptive (e.g. 'contact.md').
Change the title at the top of the new .md file but leave the layout as post. When youre done, add it to 
the menu in the _data/menu.yml by following the syntax in that file.

If you get stuck, confused or otherwise - contact Dika.