CPAC Website
============

This is the repository for the
[CPAC website](http://www.castlepointanime.com). Note that all changes
here are public and should be live on the site. Do not push to this
repo unless the information is public.

Adding a New Post
-----------------

It should be relatively easy for non-programmers to add new news
posts. You can do so on GitHub directly without using the command
line.

1. Click on the `_posts` directory.
2. In the header next to the directory name, there is a `+`
   button. (It is nearby where it says "branch: master".) Click this
   `+` button.
3. In the `Name your file...` box, name your post
   `YEAR-MONTH-DAY-title.md`. As an example,
   `2015-02-29-ian_rubin_comes_to_cpac.md`. It is important that `.md`
   is the file extension and that the date of the post is in front.
4. In the big text box, first make a header for the post. Check
   existing posts for how it should look, or take a look at the
   [Jekyll documentation](http://jekyllrb.com/docs/frontmatter/) for
   more information. Make sure to set one or more categories based on
   the page it will show up on.
5. Below the header, write your actual post using
   [Markdown](http://daringfireball.net/projects/markdown/).
6. Save the file and make a new pull request using the green button.

The webmaster will review your post, check to make sure it does not
break the site, and then deploy it.

Site Layout
-----------

The site is made using Jekyll, so the layout is standard. Read the
Jekyll docs for more information.

The main HTML page is in `_layouts/default.html` (for pages, see
`_layouts/page.html`, which extends the default). From there, the
default layout includes a number of widgets, such as the navigation
and sidebar, from the `_includes` directory.

Deployment to S3 is done using the s3_website gem. See
`s3_website.yml` for the deploy configuration. We use the dotenv gem
to load AWS credentials, so you have to put your credentials in a
`.env` file in order to deploy. Do not commit the `.env` file to the
repository (it is .gitignore'd).
