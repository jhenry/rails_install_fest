
## Setting up our environment

Start the db (sqlite3 is not installed by default)

	$ pg_ctl start -w 

Set the db connection

	$ cp sample/config/database.yml instablog/config/ 


## Creating a blog in 5 steps

We're going to start by creating a blog, in less than 5 steps.  Before we begin, we'll want to open up a terminal.

1. First, create a new rails app:

	$ rails instablog

2. Next, we are going generate some of the code and prepare some database tables to get us started. 
	
	$ cd instablog
	$ script/generate scaffold Post title:string body:text

3. We have created a basic structure for our application, but we still need to actually create the database tables before moving forward.

	$ rake db:migrate
	
4. Now, let's start up the web server and see what we have created.

	$ script/server

Loading http://localhost:3000/posts brings us to the blog we just built.  Try adding a new post.  

## Modifying the view

Table based layouts are so Twentieth Century.  Let's replace those tables with, header and paragraph tags.

1. Open up app -> views -> posts -> index.html.erb
2. Remove table tags and replace with headers and paragraphs.
3. Save and reload page.

## Adding validation

We want to make sure our authors are not forgetting important items, such as titles.  Rails makes this pretty easy to do.

1. Open app -> models -> post.rb
2. Add the line:

	<pre>validates_presence_of :title, :message => "can't be blank"</pre>
	
Try adding a new post, and leaving the title blank.  	

## Let there be comments

Lets get wild and add a comment feature.

## References

Fabio Akita's "[The First Rails 2.0 Screencast](http://www.vimeo.com/425800 "The First Rails 2.0 Screencast on Vimeo")" is a more robust version of what we've done today.  The basic structure of this outline is based on this video.  




