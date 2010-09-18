---
layout: master
title: Welcome
---

This is a template for your app's documentation (we hope your app has [CloudApp](http://getcloudapp.com/) support built in — it really should). Collaborative writing and constant updates have to be well supported when it comes to maintaining technical documentation.

We chose [Git](http://git-scm.com/), [Jekyll](http://github.com/mojombo/jekyll/) and [SASS](http://sass-lang.com/) to get the job done. If you have never heard of Jekyll or SASS don't worry, it's very easy to get up and running. Should you be unfamiliar with Git this might not be the right thing for you.

##Writing content

Documentation consists of separate Markdown files placed inside `_posts`. You might want to take a look at a our examples. All posts are categorized and available from the sidebar.

The available categories can be found in `_layouts/master.html`. It's as simple as adding another item to that list to create a new category. To assign a post to a specific category just include it in the post's configuration.

This is what the typical configuration for a post looks like:

    ---
    layout: master
    title: Document Title
    categories: category_one category_two
    ---

We think keeping your documentation in plain text files is awesome:

- You can use your favorite [TextEditor](http://macromates.org/) to write posts.
- The generated markup is concise thanks to [Markdown](http://daringfireball.net/projects/markdown/).
- Collaboration with your team is easy and versioning is built right in.
- You can use your precious time writing posts instead of fiddling with a database.

##Deploying

Deploying is extremely easy. We recommend [Heroku](http://heroku.com/) or [Github](http://github.com/) but anything that can run [Rack](http://github.com/bry4n/rack-jekyll/) applications will work.

###Heroku

Sign up for a **free** Heroku account and read the [Quickstart Guide](http://docs.heroku.com/quickstart/). Once you know what you are doing simply follow the steps below.

Generate your Jekyll site locally (Heroku is a [read-only file system](http://docs.heroku.com/constraints#read-only-filesystem)) and make sure your SASS stylesheets are up to date:

    cd my_doc_directory
    compass watch
    jekyll

Turn the directory into a git repository:

    git init && git add .

Commit your changes and get ready to deploy:

    git commit -m "my documentation is ready"

Create the Heroku app:

    heroku create

Push to Heroku:

    git push heroku master

###Github

Deploying to Github is even easier. All you need to do is create a [Github Page](http://pages.github.com/). Some of the files included in this repository are not necessary for this. You can remove the following files (they are only included to make a Heroku deploy easy):

    config.rb
    config.ru
    Gemfile
    Gemfile.lock
