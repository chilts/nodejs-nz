# http://nodejs.nz/

A site for promoting Node.js in New Zealand.

## Contributing ##

Firstly, check out the repo:

```sh
$ git clone git@github.com:chilts/nodejs-nz.git
$ cd nodejs-nz
```

You will need both `node` and `npm` installed. You also need hexo installed globally:

```sh
$ npm install -g hexo-cli
```

Head into the `site` directory and install all other npm dependencies:

```sh
$ cd site
$ npm install
$ make generate
$ xdg-open public
```

Once everything has been generated, add it all (including `site/public`) and send a PR.

The reason the generated docs are checked in are twofold: (1) any diffs in the generated site can be seen in git and
therefore it's easier to tell if the site hasn't been generated correctly or something untoward went wrong, and (2) the
server doesn't have anything like node, npm or hexo installed and is pretty simple.

## About ##

This site uses [Hexo](http://hexo.io/) to generate a static version of the site. It was created with the following
command:

```sh
$ mkdir nodejs-nz
$ hexo init site
$ cd site
$ npm install
$ hexo generate
```

Since the site is generated locally and pushed to the server we don't add `public` to `.gitignore`.

## License ##

The MIT License (MIT). Copyright 2015 Andrew Chilton.

(Ends)
