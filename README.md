# http://nodejs.nz/

A site for promoting Node.js in New Zealand.

## Contributing ##

Pre-requisites: You will need both `node` and `npm` installed.

Firstly, check out the repo:

```sh
$ git clone git@github.com:chilts/nodejs-nz.git
$ cd nodejs-nz
```

Now, head into the `site` directory and install all the npm packages we need:

```sh
$ cd site
$ npm install
```

At this point, you can make the changes you want to the site. Then to regenerate:

```sh
$ make generate
$ make server
```

In your browser, head to `http://localhost:4000` and check everything looks as it should.

Once you're happy with the changes, just add and commit the changes to the `src/` directory (and anything else) but do
not add any changes within `htdocs/`. This way I can merge changes and regenerate and push myself prior to
releasing. This makes it easier if there are two PRs incoming at the same time.

The reason the generated site is checked in are twofold: (1) any diffs in the generated site can be seen in git and
therefore it's easier to tell if the site has or hasn't been generated correctly or if something untoward went wrong,
and (2) the server doesn't have anything like node, npm or hexo installed and is pretty simple.

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
