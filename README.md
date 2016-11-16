# How-to

Needs [Node.js](https://nodejs.org/) and [Harp](https://harpjs.com).

```shell
$ npm install -g harp
$ git clone https://github.com/aentan/rffxv-theme.git
$ cd rffxv-theme
$ harp server
```

Then go to `http://localhost:9000/` to see the site.

## Styling

Write your CSS in `styles/style.scss`. Harp will serve it as CSS in runtime. Write SCSS if you know how, to take advantage of it.

## Compiling

```shell
$ harp compile ./ docs
```

This compiles the project into the `docs` directory. The CSS that should be used for the reddit stylesheet is in `docs/styles/style.css`.

## Deploy & Test

```shell
$ git push
```

Github pages is set up for the `master` branch and `docs` folder of the repository. Simply `push` and you will see the site live at [aentan.github.io/rffxv-theme/](https://aentan.github.io/rffxv-theme/).