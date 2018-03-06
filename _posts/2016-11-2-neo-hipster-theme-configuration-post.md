---
layout: post
title: "Neo-HPSTR Theme Configuration"
description: "Tutorial on setting up the Neo-Hipster Jekyll Theme"
tags: [jekyll, theme, tutorial, neo-hipster, neo-hpstr, disqus, open graph, developer, mmistakes, install, configuration]
comments: true
image:
  background: v4truth.png
---

## Neo-HPSTR Features

* Neo-HPSTR is a fully functional Jekyll Blog theme created by Michael Rose

<a href="https://mademistakes.com/support/"><img style="border:0px;" src="http://images.webestools.com/buttons.php?frm=1&btn_type=16&txt=Support%20the%20Developer" onmouseover="this.src='http://images.webestools.com/buttons.php?frm=2&btn_type=16&txt=Support%20the%20Developer'" onmouseout="this.src='http://images.webestools.com/buttons.php?frm=1&btn_type=16&txt=Support%20the%20Developer';" alt="Support%20the%20Developer" /></a><script type="text/javascript">img=new Image();img.src= "http://images.webestools.com/buttons.php?frm=2&btn_type=16&txt=Support%20the%20Developer";</script>

* Modern and minimal design.
* Responsive templates for post, page, and post index `_layouts`. Looks great on mobile, tablet, and desktop devices.
* Gracefully degrades in older browsers. Compatible with Internet Explorer 8+ and all modern browsers.  
* Sweet animated menu with support for drop-downs.
* Optional [Disqus](http://disqus.com) comments and social sharing links.
* [Open Graph](https://developers.facebook.com/docs/opengraph/) and [Twitter Cards](https://dev.twitter.com/docs/cards) support for a better social sharing experience.
* Simple [custom 404 page](http://mmistakes.github.io/hpstr-jekyll-theme/404.html) to get you started.
* [Syntax highlighting](http://mmistakes.github.io/hpstr-jekyll-theme/code-highlighting-post/) stylesheet to make your code examples look snazzy
* [Available in Spanish](https://github.com/cruznick/hpstr-jekyll-theme/tree/es). Thanks [@cruznick](https://github.com/cruznick)!



## Download the Theme
Navigate to your Desktop directory (Feel free to use any directory you want)

```
userone@laptop:~/Development/tutorials$ cd ~
userone@laptop:~/Desktop$
```

<a href="https://github.com/mmistakes/hpstr-jekyll-theme/archive/master.zip"><img style="border:0px;" src="http://images.webestools.com/buttons.php?frm=1&btn_type=16&txt=Download%20the%20Theme" onmouseover="this.src='http://images.webestools.com/buttons.php?frm=2&btn_type=16&txt=Download%20the%20Theme'" onmouseout="this.src='http://images.webestools.com/buttons.php?frm=1&btn_type=16&txt=Download%20the%20Theme';" alt="Download%20the%20Theme" /></a><script type="text/javascript">img=new Image();img.src= "http://images.webestools.com/buttons.php?frm=2&btn_type=16&txt=Download%20the%20Theme";</script>

Click the button or enter the following commands into the terminal.

```
wget https://github.com/mmistakes/hpstr-jekyll-theme/archive/master.zip

```

Once the theme finishes downloading you need to extract it into the you want to work in.  
```
unzip ~/Desktop/hpstr-jekyll-theme-master/
```

If you did everything correctly you should now have a copy of Neo-HPSTR on in a folder called hpstr-jekyll-theme-master on your desktop.  The next section of the tutorial deals with configuring theme.  if you have not already installed jekyll and it's dependencies please do that before preceeding. Link to [Jekyll Install Tutorial]( http://localhost:4000/neo-hipster-theme-configuration-post/)


## Basic Setup and Configuration

After downloading Neo-HPSTR you can begin configuring the theme so it will run properly in Jekyll.  Open your terminal and navigate to the hpstr-jekyll-theme-master/ you created in the previous section of this tutorial. If you unipped it on your Desktop enter the following commands into the terminal.  

```
userone@laptop:~/Desktop$ cd ~/Desktop/hpstr-jekyll-theme-master/
userone@laptop: ~/Desktop/hpstr-jekyll-theme-master$
```

Next you need to make install Bundler and all theme dependencies by entering the folowing commands into the
terminal.

```
userone@laptop: ~/Desktop/hpstr-jekyll-theme-master$ gem install bundler
```

Now to install the Neo-HPSTR's dependencies


```
userone@laptop: ~/Desktop/hpstr-jekyll-theme-master$ bundle install
```


## Customizing the Theme

Once you have installed the theme's dependencies you need to edit the ==_config.yml== YAML file to personalize your site.  Open the file with your favorite text editor and enter your personal information.

```
title:            Enter Your Sites Title
description:      Provide a short description of your blog
disqus_shortname: We will deal with Disqus in the next section leave blank for now.

url: http://localhost:4000 The url must be set to localhost:4000 when running it locally and you will need to change this to your websites address before deploying our blog.  

Owner/author information You must provide information for the name, bio, and email variables or some sections of the site will not function correctly.   
owner:
  name:           Enter Your Name
  avatar:         avatar.jpg
  bio:            Enter a short bio about yourself.
  email:          Enter your email
  # Social networking links used in footer. Update and remove as you like.
  github:         github username
  keybase:        keybase username
  stackexchange:  you get the idea
  linkedin:
  instagram:   
  google_plus:    for google plus make sure you put a + infront of your username


timezone:    Change if not are not in the America/New_York time zone.
```

After editing the ==_config.yml== file make sure you save your changes before proceeding to the next step.  


## Running Jekyll

The preferred method for running Jekyll is with ==bundle exec jekyll "command option"==, but if you’re willing to deal gem conflicts feel free to go cowboy with a ==jekyll build== or ==jekyll serve==.  Once you have dealt with gem conflicts I assure you, you will have no problem typing a few more characters and launching the site using == bundle exec jekyll serve==
That said, enter the following commands into the terminal and launch the site on your local server (http://localhost:4000).

In some cases you may want to rebuild your blog before launching it.  To do this you just need to run ==bundle exec jekyll build== before launching the site.  

```
userone@laptop: ~/Desktop/hpstr-jekyll-theme-master$ bundle exec jekyll build
```

```
userone@laptop: ~/Desktop/hpstr-jekyll-theme-master$ bundle exec jekyll serve
Configuration file: /home/userone/Development/jajb-master/_config.yml
            Source: /home/userone/Development/jajb-master
       Destination: /home/userone/Development/jajb-master/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 1.003 seconds.
 Auto-regeneration: enabled for '/home/userone/Development/jajb-master'
Configuration file: /home/userone/Development/jajb-master/_config.yml
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

If the serve command executes without any errors you should be able to open up a browser and got to http://localhost:4000) and your new blog should load. If the command executes without an error but does not load in your browser the problem most likely is due to a misconfigured _config.yml file.  To fix this open the _config.yml file and make sure the url: setting is set to http://localhost:4000.  

Good Job!  You can now see the fruits of your labor and naviate the default posting included in with the theme.  In the next section of this tutorial I will show you how to set up backgrounds, load avatars and wire up the advanced features in this blog.  

If you made it this far into the tutorial and plan on using the theme for your blog then tell the developer thank you by making a donation.  Even if it's only a few bucks I am sure it will be appreciated and if you wondering I don't know the theme's developer and will not benefit financially whatsoever from your donation.  However if you do donate all of us could benefit in the future because the developer might just put out another dope theme or some other FOSS for the world to use.  

Information should be free not trademarked and copy written.  


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
