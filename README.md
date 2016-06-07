![logo](https://github.frapsoft.com/top/npm-logo.png)

# Publishing NPM Packages for Developers [![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=102)](https://github.com/ellerbrock/open-source-badge/) [![Gitter Chat](https://badges.gitter.im/frapsoft/frapsoft.svg)](https://gitter.im/frapsoft/frapsoft/)

Introduction how to [publish](https://docs.npmjs.com/getting-started/publishing-npm-packages) npm modules.

## Resources

- [Node.js for Developers](https://github.com/ellerbrock/node.js-for-developers)
- [NPM Developer Guide](https://docs.npmjs.com/misc/developers)
- [Common.js Module Specs](http://www.commonjs.org/specs/modules/1.0/)
- [NPM Module Best Practices](https://github.com/mattdesl/module-best-practices)
- [Faster & Cleaner Module Workflow](https://mattdesl.svbtle.com/faster-and-cleaner-modules)
- [Getting Started with Node and NPM](https://github.com/Microsoft/nodejs-guidelines/blob/master/getting-started.md)
- [Choosing a licence for your Open Source Project](https://github.com/ellerbrock/tutorial-choosing-open-source-licence)
- [Awesome NPM](https://github.com/sindresorhus/awesome-npm)
- [Awesome Node.js](https://github.com/sindresorhus/awesome-nodejs)
- [Awesome TypeScript](https://github.com/ellerbrock/awesome-typescript)
- [Interactive Guide for exploring package.json](http://browsenpm.org/package.json)
- [10 Cool Things You Probably didn't realize npm could do](http://blog.izs.me/post/1675072029/10-cool-things-you-probably-didnt-realize-npm-could-do)
- [Semantic Versioning](http://semver.org/)
- [Creating and Publishing a Node.js Module](https://quickleft.com/blog/creating-and-publishing-a-node-js-module/)
- [Creating Node.js modules](https://docs.npmjs.com/getting-started/creating-node-modules)
- [How to write Node.js Modules](http://www.hacksparrow.com/how-to-write-node-js-modules.html)
- [module-generator](https://github.com/hughsk/module-generator)
- [Modules 1.1 Wikipedia](http://wiki.commonjs.org/wiki/Modules/1.1)

## Installation

**OS X**

with [curl](https://curl.haxx.se/)

```
curl http://npmjs.org/install.sh | sh
```

or with [Homebrew](http://brew.sh/)

```
`brew update && brew install node`
```

If you want to choose [another node version](https://github.com/Homebrew/homebrew-versions) (in this example the long-term support for node 4) you can do so:

```
brew tap homebrew/versions
brew install homebrew/versions/node4-lts
brew link --overwrite node4-lts
```

**Linux**

```
curl http://npmjs.org/install.sh | sudo sh
```

or on a apt based linux version via

```
apt-get update && apt-get install npm
```

## Configuration

```
npm set init.author.name "Your Name"
npm set init.author.email "you@example.com"
npm set init.author.url "http://yourblog.com"

npm adduser
```

<https://docs.npmjs.com/cli/adduser>

Then create a `package.json` and publish it:

```
cd /path/to/your-project
npm init

npm install -g pakmanager
# this shows you dependencies as you `require`d them

pakmanager deps
# now edit `package.json` and add any deps you forgot about

npm publish ./
```

<https://docs.npmjs.com/files/package.json><br>
<http://browsenpm.org/package.json>

## Beta and Release versions

If you don't want something to install by default

`npm publish ./ --tag beta` <<https://docs.npmjs.com/cli/publish>

If you published a bugfix as v1.0.7 and need to set v1.1.3 back to latest

<https://docs.npmjs.com/cli/publish>

```
git checkout v1.0.7
npm publish ./

git checkout v1.1.3
npm tag foobar@1.1.3 latest
```

<https://git-scm.com/docs/git-checkout><br>
<https://docs.npmjs.com/cli/publish><br>
<https://docs.npmjs.com/cli/tag>

## Remove a package from the registry

`npm unpublish package`

Its considered bad behavior to remove versions of a library others depending ong. A better way to is to mark the package as deprecated

<https://docs.npmjs.com/cli/unpublish>

`npm deprecate package`

<https://docs.npmjs.com/cli/deprecate>

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

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />

This work by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/ellerbrock/" property="cc:attributionName" rel="cc:attributionURL">Maik Ellerbrock</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.