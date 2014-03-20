---
layout: post
title: "From Zero to Octopress in 4 Hours"
date: 2014-02-15 09:01:20 +0800
comments: true
categories: tech life 
---
After sitting on the todo list for about an eternity, I've finally knuckled down to push this blog onto the interwebs. This supersedes my old blog - *Ghettotoyota.com*, dating way back to high school / college years. I dedicate this new blog to you, 1988 Toyota Tercel; may you continue to live your [*Initial D*](http://en.wikipedia.org/wiki/Initial_D) dreams in Thug Mansion.

One of the most beautiful things about the internet is the sheer volume of easily accessible knowledge. In the spirit of contributing to that idea, what follows is the quick mind dump of how I brought this baby online. 

##Hours 1 and 2

Let's do it. What are the criteria? 

1. Gotta be free.
2. No ads.
3. Flexible layout that allows for themes because my CSS/LESS skills ain't paying the bills yet. 
4. Something that's hackable so I can get my hands dirty and do something about #3
5. Not blocked by the Chinese government (damn you [GFW](http://en.wikipedia.org/wiki/Golden_Shield_Project))

*Blogger*, *Tumblr* and *Wordpress* were out. *Posterous* had gone to a better place, and its replacement wasn't free. This left the following:

* [Ghost.js](http://www.ghost.org) 
* [Octopress](http://www.octopress.org)

Ghost is fresh off the kickstarted press and looked awesome, but a stable solution isn't yet available for Heroku. Azure charges monthly fees, and I've used up my free year of AWS running an [AWS VPN](http://tutorials.eriksoderstrom.com/16/create-a-personal-vpn-with-amazon-ec2/) while here in China. 

Octopress is free and can be hosted off of your own Github account. It's well documented and built on [Jekyll](http://jekyllrb.com/), which also fits with my long term goals of [learning Ruby](http://ruby.railstutorial.org).

All aboard the Octopress train.

##Hour numero 3

A slew of good Octopress tutorials exist on the net. [Paul Sturgess's](http://paulsturgess.co.uk/blog/2013/04/24/hello-octopress-and-github-pages/) was a great help, as was [Moncef Belyamani's](http://www.moncefbelyamani.com/how-to-install-and-configure-octopress-on-a-mac/). 

Moncef recommended to create a separate Ruby gemset for the Octopress installation. It seems that the purpose of a gemset is to keep your gems (libraries?) for one app isolated from the required gems for other apps in the case that your apps require differing gem versions. 

Though, I did create a separate gemset for Octopress, I must have screwed something up because I ran into the following error when running anything using `rake`:

```
rake aborted!
You have already activated rake 0.9.6, but your Gemfile requires rake 0.9.2.2.
Prepending `bundle exec` to your command may solve this.
```

Lo and behold, running `bundle exec` did indeed fix the issue, but if bundle automagically selects the right gems for the job, why do we need to segregate things with gemsets? Furthermore, my attempts to remove the offending rake version with `gem uninstall` failed. Wack.  

##Hour 4

Mo' coding mo' problems. When attempting to push to Github, I was thrown this nice message: 

```
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'git@github.com:soltrain/soltrain.github.io.git'
hint: Updates were rejected because the tip of your current branch is behind its remote counterpart.
Merge the remote changes (e.g. 'git pull') before pushing again.
```

Unfortunately, I've forgotten the root cause for the error, but the amazing box o' knowledge that is StackOverflow [came through with a solution](http://stackoverflow.com/questions/19619280/octopress-pushing-error-to-github). 

Success! 

Implementing themes turned out to be a piece of cake. Choosing the theme that best represents an extension of myself on the web, however… well, we'll just leave those details out of the report. 

##Thoughts

Technical trips aside, making Octopress run took less time than expected. There's still some work and tweaking to be done but it's a start. 

Not sure what the process flow will look like for image uploads - it appears some host on Github, others Flickr, still others, Dropbox. 

Todo:

1. Figure out images
2. Set up custom domain
3. Add related posts sidebar
4. …
5. Profit. 



















 



