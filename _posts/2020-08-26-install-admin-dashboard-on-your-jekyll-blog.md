---
title: Install admin dashboard on your Jekyll blog
layout: post-right-sidebar
categories:
- GitHub
- Jekyll
image: assets/images/jekyll-admin.png
featured: false
---

One major problem users face with the Jekyll blog is adding new posts. While writing a new post using markdown language, adding a new image or formatting the blog post could be difficult.

Admin dashboard was one standout feature for WordPress which made life simple. Especially the bloggers who migrate from wordpress to Jekyll find this as a disadvantage.

But there is an option to add an admin dashboard to your Jekyll blog.

1. Open Jekyll directory
2. Open  config.yml file in any text editor and add the below command under plugins and save it.

		`- jekyll-admin`
			
	![]({{ 'assets/images/post/jekyll-admin-1.png' | relative_url }})

3. Open 'GemFile' in any text editor and add the below command under 'group :jekyll_plugins do'.
		
			`gem "jekyll-admin"`
			
	![]({{ 'assets/images/post/jekyll-admin-2.png' | relative_url }}) 
			
4. Open the command prompt and navigate to your jekyll blog directory and execute the below command.

		`bundle exec jekyll serve`
		
	![]({{ 'assets/images/post/jekyll-admin-3.png' | relative_url }})
		
		Now this will deploy your blog in localhost.
		
5. Open any web browser and navigate to http://localhost:4000/admin or http://127.0.0.1:4000/admin to view the admin dashboard.

     ![]({{ 'assets/images/post/jekyll-admin-4.png' | relative_url }})
		 
6. Click on Posts in the left sidebar to create a new post. Input all the necessary details and click on create.

     ![]({{ 'assets/images/post/jekyll-admin-5.png' | relative_url }})
			
			
7. Now navigate to http://localhost:4000/ or http://127.0.0.1:4000 to view your blog and the post you have created will be visible in the blog.

	![]({{ 'assets/images/post/jekyll-admin-7.png' | relative_url }})
