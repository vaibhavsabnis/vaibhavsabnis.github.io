---
layout: page
permalink: /techdocs/
---

## _Steps to install and run Jekyll site locally_

Detailed installation instructions are on git [site](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll). This is a boiled-down version for quick reference.

1. Install Ruby 2.7.* from Ruby installer  
    a. Pick the right OS environment installer [Windows](https://rubyinstaller.org/downloads/).  
    b. Make sure to click on `ridk install` on the last page of the installation wizard.  
    c. Then automatically cmd installer comes up,  type  all the 3 MSYS2 options one-by-one on it. 

2. Install Bundler from Bundler site  (the Bundler gets auto installed if ruby 2.7.* + is installed). 

3. Open cmd and install Jekyll by running `gem install jekyll bundler` // this will install the latest version of Jekyll on the machine. For me it installed ver 4.2.0 

4. For a new repo, go to the cloned git repository folder on your local machine.  
    a. run `bundle init` --> this creates a new Gemfile. If you are pulling from GIT (an existing Gemfile), then this is **NOT needed**

5. Some gems may be missing so run `bundle install `. You can do that from VSCode Terminal
6. Run `bundle update github-pages` . This setups the environment from your repository directory and then you can start your server on port 4000
7. Run `bundle exec jekyll serve`

Access your site on [localhost:4000](http://localhost:4000/)
#
## _How to copy theme locally and convert the site to use "regular" theme_ 
1. Run`bundle info --path minima` gives you the path to where the theme files are stored. Contents are in _includes, _layout, _sass, _assets folder. Copy over the necessary folder (keep structure intact in the target). This acts like an typical override function. 
2. If you want to stop using minima theme then you have to copy all the above folders and then run following steps  
    1. Remove the configuration from _config.yml 
    2. Remove the corresponding theme definition from Gemfile 
    3. run `bundle update` to update the gems based on above to config changes 


## _To get a "_site" folder_ when doing local development_

Run `bundle update jekyll build`


