---
layout: post
title: "Installing Jekyll"
description: "Examples and code for displaying images in posts."
tags: [jekyll, install, tutorial, ruby, gem, bundle]
comments: true
image:
  background: 18f3be9e.png

---

## Installing Jekyll 3.0+

Over the past few months I have spent countless hours scouring the web for tutorials that will help solidify my web develoment skills. The internet offers many free tutorials on just about every topic you can think.  After a few hours of searching and start or restarting variuos tutorials I figured out that not all web tutorials are created equal.  In light of this I thought I'd take the time to create a few up to date (As of 10/15/2016) tutorials that may help other web development students steer clear of google rabbit holes and stackoverflow loops.  

Before I start (and before you comment) I'd like to say that like anything else in life there are many ways to reach any desired end and that I am going to focus on what worked for me. If you choose to provide constructive criticism please take the time to explain why your way worked better for you so we all can learn.

 OK, let's get started.


## Jekyll Dependencies

If you wanna create a simplistic but powerful blog like this one the first thing you are are going to have to do is make sure you have the tools to do the job.

* Ruby (including development headers, v1.9.3+ for Jekyll 2 and v2+ for Jekyll 3)
* RubyGems
* NodeJS
* Python 2.7 (for Jekyll 2 and earlier) or Python 3+ for Jekyll 3+)

First you will need to check and see if you have Ruby installed. Open your terminal and run.

```
userone@laptop:~/Desktop/$ ruby -v
ruby 2.3.0p0 (2015-12-25) [x86_64-linux]

```
If it returns something simular then you are all good and can proceed to the next dependency. If you need to install ruby and want to install version 2.3.1 enter the following commands into the terminal

```
sudo apt-get update

sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev.

cd

git clone https://github.com/rbenv/rbenv.git ~/.rbenv

echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc

echo 'eval "$(rbenv init -)"' >> ~/.bashrc

exec $SHELL

git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build

echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc

exec $SHELL

rbenv install 2.3.1

rbenv global 2.3.1

ruby -v
```

The last step is to install the gems bundler.
```
gem install bundler
If all went well you should have both ruby and rubygems installed. Next check and see if you have Nodejs installed

```
userone@laptop:~/Desktop/$ nodejs --version
v6.9.2

```
If it returns something like ruby 4.6.1 then you are all good and can proceed to the next dependency on the list. If you need to install nodejs 4.6.1 enter the following commands into the terminal.

```
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
nodejs -v
```

Now run the following command to make sure it installed correctly.

```
userone@laptop:~/Desktop/$ nodejs --version
v6.9.2
```
If it returns the version you installed move on to last dependency.

The final dependecy is Python and since it comes pre-installed on all Ubuntu 14.04 systems. Check and make sure your have a working version by running the following command.

```
userone@laptop:~/Desktop$ python
Python 3.4.3 (default, Nov 17 2016, 01:08:31)
[GCC 4.8.4] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

You should have all the dependencies installed and be able to install Jekyll without any errors.


## Install Jekyll

Simply run the following command.

```
userone@laptop:~/Desktop$ gem install bundler jekyll
```

Now that Jekyll is installed you can start a new project by running the following command.

```
userone@laptop:~/Desktop$ jekyll new "name of your project without "" "
userone@laptop:~/Desktop$ cd "name of project"
userone@laptop:~/Desktop$ bundle exec jekyll serve
```

Now head over to <a href="http://jekyllrb.com/docs/installation/">Jekyll's Documentation page</a> and familiarize yourself with the program. This will be the starting point in the next entry of this the tutorial. Thanks again for following along and if you have questions or comments feel free to leave a comment.

{% if page.comments %}
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = '//jajb.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}
