# How-to

Needs [Node.js](https://nodejs.org/) and [Harp](https://harpjs.com).

```shell
$ npm install -g harp
$ git clone https://github.com/voicrose/rffxv-theme.git
$ cd rffxv-theme
$ harp server
```

Then go to [http://localhost:9000/](http://localhost:9000/) to see the site.

## Styling

Write your CSS in `styles/style.scss`. Harp will serve it as CSS in runtime. Write SCSS if you know how, to take advantage of it.

## Compiling

```shell
$ harp compile ./ docs
```

This compiles the project into the `docs` directory. The CSS that should be used for the reddit stylesheet is in `docs/styles/style.css`.

The SASS preprocessor in Harp.js appears to add some weird properties to the generated CSS, which fails in Reddit's CSS Linter. What I currently do to remove these unwanted styles is to simply run and Find & Replace with regex.

Simply open `docs/styles/style.css`, find `-webkit-box-\b(pack|align):center;` and replace with an empty string. Then copy and paste into Reddit's CSS editor.

## Deploy & Test on Dummy Pages

```shell
$ git push
```

Github pages is set up for the `master` branch and `docs` folder of the repository. Simply `push` and you will see the site live at [voicrose.github.io/rffxv-theme/](https://voicrose.github.io/rffxv-theme/).