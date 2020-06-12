---
layout: post-right-sidebar
title:  "How to use Jenkins for Python unit testing?"
categories: [ Python, Jenkins ]
image: assets/images/post/python-jenkins.png
featured: false
---
Jenkins is an open source continous integration tool. It is used to automate the tasks such as building, testing and deployment of code.
In this post, I will explain you how to configure Jenkins to do unit testing with Python.

<b>Download and Install Jenkins</b>

Jenkins is cross platform and can be used on windows, Linux, Mac OS and Solaris enviornments.  Download Jenkins from [Official Site][jekyll-jenkins] and install the version corresponing to yur operating system.
Once the installation is completed, the jenkins will run automatically on http://localhost:8080/, the page will open in your default browser.


![alt text]({{site.baseurl}}/assets/images/post/jenkins-1.png)


get the default password from the file specified and paste it in the password field.

`[Tip]: You can copy paste the entire URL in the browser itself to get the password`

In the next screen, select 'Install suggested plugins'. 

Once the suggested plugins are installed we need to install a plugin which for Python test case. [ShiningPanda][jekyll-shiningpanda] is one such plugin. 

Once you complete the set up of Jenkins, from Dashboard, choose `Manage Jenkins` from left side bar.

Navigate to `Manage Jenkins > Manage Plugins > Available` .

In the search bar, type 'ShiningPanda' and install without restart .

![alt text]({{site.baseurl}}/assets/images/post/jenkins-2.png)


Now from the Dashboard, navigate to `Manage Jenkins > Global Tool Configuartion > Python`.

Enter the name as 'python' and give the path of the python installation in the 'Home or executable field'.

![alt text]({{site.baseurl}}/assets/images/post/jenkins-3.png)

Now you need to install [nose][jekyll-nose] package on your local machine. nose extends unittest to make testing easier. Open command prompt and type in the following.

`pip install nose`

<b>Set up new project in jenkins</b>

Go back to Jenkins Dashboard and select 'New Item'. Enter your project name and choose freestyle project.

![alt text]({{site.baseurl}}/assets/images/post/jenkins-4.png)

In the next screen, under Build - choose Python builder.

In command filed type `nosetests <path of your python code>`

![alt text]({{site.baseurl}}/assets/images/post/jenkins-5.png)

Once it is completed, click on build now. The build will start and once it is completed you can view the result for console correposning to each version.

![alt text]({{site.baseurl}}/assets/images/post/jenkins-5.png)


If you want a sample python code for unit test, please clone it from my [Github][jekyll-github] repository. 

[jekyll-jenkins]:https://www.jenkins.io/
[jekyll-shiningpanda]:https://plugins.jenkins.io/shiningpanda/
[jekyll-nose]:https://nose.readthedocs.io/en/latest/
[jekyll-github]:https://github.com/akhilgeo