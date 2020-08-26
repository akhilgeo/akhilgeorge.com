---
title: Create a Jekyll blog using command line on localhost server
layout: post-right-sidebar
categories:
- GitHub
- Jekyll
image: assets/images/post/jeykll.png
featured: false
---

Jekyll is known for building static blogs to be hosted on Github.  What makes it special is its minimalist design and fast page load speeds. 

Unlike Wordpress, Jekyll does not have any database in the backend, which is one of the main reasons which make the blogs built on jekyll faster.

Also, Jekyll blogs can be hosted on Github free of cost which make it econmical when compared to wordpress. 

But setting up a jekyll blog/website for the first time  is a bit of difficult task. In this post I will explain you how to set up a jekyll blog on your localhost using command line. Before executing tthe below steps please make sure Ruby is installed in your system.


1. Open Command prompt and navigate to your directory where you want to create the jekyll files.
2. Type the below command and press enter.

	`gem install bundler jekyll`

	![]({{ 'assets/images/post/jekyll-1.png' | relative_url }})
 
	This will install the jekyll bundler to your machine.
		 
3. Now to create a new blog, type in the below commands. Replace '<blog-name>' with the name of your blog
		
	`	jekyll new <blog-name>`
	
	![]({{ 'assets/images/post/jekyll-2.png' | relative_url }})
	![]({{ 'assets/images/post/jeykll-2-1.png' | relative_url }})
	
4. Navigate to the blog directory in command promt and type in the below command to start the localhost server.
	

	`cd <blog-name>`
	
	`bundle exec jekyll serve`

	
	![]({{ 'assets/images/post/jekyll-3.png' | relative_url }})
	
	Now the blog will start running on the localhost. Open any webbrowser and goto http://localhost:4000/ or http://127.0.0.1:4000 to view the jeykll blog you have created through command prompt.
	
	![]({{ 'assets/images/post/jekyll-4.png' | relative_url }})
