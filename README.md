![logo](https://github.frapsoft.com/top/npm-logo.png)  

# Publishing NPM Packages for Developers [![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v101)](https://github.com/ellerbrock/open-source-badge/) [![Gitter Chat](https://badges.gitter.im/frapsoft/frapsoft.svg)](https://gitter.im/frapsoft/frapsoft/)

Introduction how to [publish](https://docs.npmjs.com/getting-started/publishing-npm-packages) npm modules.  


## Installation

**OS X**

with [curl](https://curl.haxx.se/)

    curl http://npmjs.org/install.sh | sh
    
or with [Homebrew](http://brew.sh/)
    
    `brew update && brew install node`  

If you want to choose [another node version](https://github.com/Homebrew/homebrew-versions) (in this example the long-term support for node 4) you can do so:
 
	brew tap homebrew/versions
	brew install homebrew/versions/node4-lts
	brew link --overwrite node4-lts    
    

**Linux**

    curl http://npmjs.org/install.sh | sudo sh
    
or on a apt based linux version via

	apt-get update && apt-get install npm

	
	
## Configuration

    npm set init.author.name "Your Name"
    npm set init.author.email "you@example.com"
    npm set init.author.url "http://yourblog.com"

    npm adduser
    
<https://docs.npmjs.com/cli/adduser>

    
Then create a `package.json` and publish it:

    cd /path/to/your-project
    npm init

    npm install -g pakmanager
    # this shows you dependencies as you `require`d them
    
    pakmanager deps
    # now edit `package.json` and add any deps you forgot about

    npm publish ./

<https://docs.npmjs.com/files/package.json>  
<http://browsenpm.org/package.json>  


## Beta and Release versions

If you don't want something to install by default

`npm publish ./ --tag beta` <https://docs.npmjs.com/cli/publish
   
If you published a bugfix as v1.0.7 and need to set v1.1.3 back to latest  

<https://docs.npmjs.com/cli/publish>

```
git checkout v1.0.7
npm publish ./
   
git checkout v1.1.3
npm tag foobar@1.1.3 latest
```

<https://git-scm.com/docs/git-checkout>  
<https://docs.npmjs.com/cli/publish>  
<https://docs.npmjs.com/cli/tag>

## Remove a package from the registry

`npm unpublish package`  

Its considered bad behavior to remove versions of a library others depending ong.
A better way to is to mark the package as deprecated  

<https://docs.npmjs.com/cli/unpublish>

`npm deprecate package`  

<https://docs.npmjs.com/cli/deprecate>


## Resources

* <https://docs.npmjs.com/misc/developers>
* <https://github.com/Microsoft/nodejs-guidelines/blob/master/getting-started.md>
* <https://github.com/sindresorhus/awesome-nodejs>
* <http://browsenpm.org/package.json>
* <http://blog.izs.me/post/1675072029/10-cool-things-you-probably-didnt-realize-npm-could-do>
* <http://semver.org/>
* <http://choosealicense.com/>
### Contact / Social Media

*Get the latest News about Web Development, Open Source, Tooling, Server & Security*

[![Twitter](https://github.frapsoft.com/social/twitter.png)](https://twitter.com/frapsoft/)
[![Facebook](https://github.frapsoft.com/social/facebook.png)](https://www.facebook.com/frapsoft/)
[![Google+](https://github.frapsoft.com/social/google-plus.png)](https://plus.google.com/116540931335841862774)
[![Gitter](https://github.frapsoft.com/social/gitter.png)](https://gitter.im/frapsoft/frapsoft/)
[![Github](https://github.frapsoft.com/social/github.png)](https://github.com/ellerbrock/)

### Development by 

Developer / Author: [Maik Ellerbrock](https://github.com/ellerbrock/)  
Company: [Frapsoft](https://github.com/frapsoft/)


### License 

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />

This work by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/ellerbrock/" property="cc:attributionName" rel="cc:attributionURL">Maik Ellerbrock</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.