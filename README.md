# m-core Website

## How To Participate

You can report problems or help improve m-core.org by opening an issue or a [pull request](https://github.com/m-coin/m-core.org/compare). 

## Setting Up Your Environment

Run commands

    sudo npm i -g gulp bower browser-sync
    sudo gem install bundler

#### Build Site With Jekyll From Bundler

Make sure you have ruby and then install bundler:

    gem install bundler

Run the following command from within your local m-core.org repository: 

    bundle install
    npm install

Finally, build the website into _site/:

    bundle exec jekyll build

You can copy the output files from _site/ to the root of your web server. If you want to browse the site locally, run

    bundle exec jekyll serve

and then visit http://127.0.0.1:4000/.

## Using Rake tasks

```
$ bundle exec rake post title="title"
$ bundle exec rake page name="about.md"
$ bundle exec rake category title="Main"
$ bundle exec rake tag title="News"
```

## Using Jekyll

### Running the server:

```
$ bundle exec jekyll server
```

Access, [localhost:4000](http://localhost:4000/)

## Using Gulp

### Rum gulp

```
$ gulp
```

---

## Deploy in Github pages in 2 steps

1. Change the variables `GITHUB_REPONAME` and `GITHUB_REPO_BRANCH` in `Rakefile`
2. Run `rake` or `rake publish` for build and publish on Github

---

License
-------

Released under the terms of [the MIT license](/LICENSE) or see https://opensource.org/licenses/MIT.