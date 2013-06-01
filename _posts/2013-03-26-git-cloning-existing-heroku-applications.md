---
layout: post
title: "Git Cloning Existing Heroku Applications"
description: ""
category: Study
tags: [git, heroku]
---
{% include JB/setup %}
####To clone the source of an existing application from Heroku using Git, you could do followings:
<!--break-->
#### If you don't install heroku ,please do it first:  

>$ sudo gem install heroku  
####   Done this ,let's begin.
 
>$ heroku login  

####   There will use your heroku account and password.

>$ heroku keys:add  

#### Now you can clone the remote repository:  

>$ git clone git@heroku.com:appname.git

#### To clone the source of an existing application from Heroku using Git, use:

>$ heroku git:clone -a your_app

#### Maybe you will see the errors like this:
</br>
    Agent admitted failure to sign using the key.
    Permission denied (publickey).  
####    Don't worry,it can be solved just by:

>$  ssh-add  

####    Now,you just redo  

>$ heroku git:clone -a your_app  

####   Then,all things will be okay.
#### You may just refer to
:
<https://devcenter.heroku.com/articles/git-clone-heroku-app>