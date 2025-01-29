---
layout: post
---

Now that I have found a theme that I like, I am going to have to produce some automation to make my posting a bit easier.  Initially, this will involve a script that will create a new post branch (branch name configuration being worked on), and then create a new post file. 

The file name for posts is in the format:  '<year>-<month>-<day>-<title>.md'.

Once the file has been added and edited, I will then need to bundle it, merge the post branch into main and push to github.  Then it will be up to github to process it and post the new version of the site.  

But, before we push, it is always a good idea to be able to test the changes and ensure that things look the way we expect. This can be done by issuing the following command:

   bundle exec jekyll serve

The output will point you to the page link to view your post.


I am this much closer to having a blog of my own where I don't have to worry about ads.  Although I do need to investigate the inner workings of this Jekyll based site and see if there are things like tags, but I don't know if there are considering this is a static site.  We will find out, though.  

Till next post!
