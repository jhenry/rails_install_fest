
## Creating a blog in less than 5 steps

We're going to start by creating a blog, in less than 5 steps.  Before we begin, we'll want to open up a terminal.

1. First, create a new rails app:

	$ rails instablog

2. Next, we are going generate some of the code and prepare some database tables to get us started. 

	$ script/generate scaffold Post title:string body:text

3. We have created a basic structure for our application, but we still need to actually create the database tables before moving forward.

	$ rake db:migrate
	
4. Now, let's start up the web server and see what we have created.

	$ script/server

Loading http://localhost:3000/posts brings us to the blog we just built.  Try adding a new post.  

## Modifying the view

Table based layouts are so Twentieth Century.  Let's replace those tables with, header and paragraph tags.

## Adding validation

We want to make sure our authors are not forgetting important items, such as titles.  

## Let there be comments?

Time permitting, lets get wild and add a comment feature.

## References

Fabio Akita's "[The First Rails 2.0 Screencast](http://www.vimeo.com/425800 "The First Rails 2.0 Screencast on Vimeo")" is a more robust version of what we've done today.  The basic structure of this outline is based on this video.  




