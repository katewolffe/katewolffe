# Kate Wolffe's personal site

Built using Hyde, a brazen two-column [Jekyll](http://jekyllrb.com) theme that pairs a prominent sidebar with uncomplicated content. It's based on [Poole](http://getpoole.com), the Jekyll butler.

![Hyde screenshot](https://f.cloud.github.com/assets/98681/1831228/42af6c6a-7384-11e3-98fb-e0b923ee0468.png)


## Contents

- [Usage](#usage)
- [Options](#options)
  - [Sidebar menu](#sidebar-menu)
  - [Sticky sidebar content](#sticky-sidebar-content)
  - [Themes](#themes)
  - [Reverse layout](#reverse-layout)
- [Development](#development)
- [Author](#author)
- [License](#license)


## Usage

Hyde is a theme built on top of [Poole](https://github.com/poole/poole), which provides a fully furnished Jekyll setup—just download and start the Jekyll server. See [the Poole usage guidelines](https://github.com/poole/poole#usage) for how to install and use Jekyll.


## Options

Hyde includes some customizable options, typically applied via classes on the `<body>` element.


### Sidebar menu

Create a list of nav links in the sidebar by assigning each Jekyll page the correct layout in the page's [front-matter](http://jekyllrb.com/docs/frontmatter/).

```
---
layout: page
title: About
---
```

**Why require a specific layout?** Jekyll will return *all* pages, including the `atom.xml`, and with an alphabetical sort order. To ensure the first link is *Home*, we exclude the `index.html` page from this list by specifying the `page` layout.


### Sticky sidebar content

By default Hyde ships with a sidebar that affixes it's content to the bottom of the sidebar. You can optionally disable this by removing the `.sidebar-sticky` class from the sidebar's `.container`. Sidebar content will then normally flow from top to bottom.

```html
<!-- Default sidebar -->
<div class="sidebar">
  <div class="container sidebar-sticky">
    ...
  </div>
</div>

<!-- Modified sidebar -->
<div class="sidebar">
  <div class="container">
    ...
  </div>
</div>
```


### Themes

Hyde ships with eight optional themes based on the [base16 color scheme](https://github.com/chriskempson/base16). Apply a theme to change the color scheme (mostly applies to sidebar and links).

![Hyde in red](https://f.cloud.github.com/assets/98681/1831229/42b0b354-7384-11e3-8462-31b8df193fe5.png)

There are eight themes available at this time.

![Hyde theme classes](https://f.cloud.github.com/assets/98681/1817044/e5b0ec06-6f68-11e3-83d7-acd1942797a1.png)

To use a theme, add anyone of the available theme classes to the `<body>` element in the `default.html` layout, like so:

```html
<body class="theme-base-08">
  ...
</body>
```

To create your own theme, look to the Themes section of [included CSS file](https://github.com/poole/hyde/blob/master/public/css/hyde.css). Copy any existing theme (they're only a few lines of CSS), rename it, and change the provided colors.

### Reverse layout

![Hyde with reverse layout](https://f.cloud.github.com/assets/98681/1831230/42b0d3ac-7384-11e3-8d54-2065afd03f9e.png)

Hyde's page orientation can be reversed with a single class.

```html
<body class="layout-reverse">
  ...
</body>
```


## Development

Hyde has two branches, but only one is used for active development.

- `master` for development.  **All pull requests should be submitted against `master`.**
- `gh-pages` for our hosted site, which includes our analytics tracking code. **Please avoid using this branch.**


## Author

**Mark Otto**
- <https://github.com/mdo>
- <https://twitter.com/mdo>


## License

Open sourced under the [MIT license](LICENSE.md).

<3

## Start Message to Kate

Congrats on being done with France School Stuff. Here's a first draft of your site!

This site is a little techie, so you'll have to use a bit of that CS61A magic to make changes to it.

### Prerequisites

#### 1. Install RVM (Ruby Version Manager)

This site uses a website generator called [Jekyll](https://jekyllrb.com/) to create the html pages. But it needs a programming language called [ruby](http://tryruby.org/levels/1/challenges/0) and a tool called [bundler](http://bundler.io/) to make things work.

You can install RVM by going [here](https://rvm.io/rvm/install). Or you can just run the following command in your terminal.

```
\curl -sSL https://get.rvm.io | bash -s stable --ruby
```

#### 2. Install bundler.

```
gem install bundler
```

#### 3. Download your website's code

This whole site lives [here, on Github.](https://github.com/katewolffe/katewolffe.github.io). You may have to do a little refresher (or maybe a complete refresher) on git in order to make changes. It'll be frustrating at first, but you'll get it!

Here's a quick course on how to use git (and Github):
[Github's tutorial](https://guides.github.com/activities/hello-world/)

### Making changes

Look to the left - There's your face and name. You can change both of those by following the tutorial above to clone [this repository](https://github.com/katewolffe/katewolffe.github.io), make a change, and push.

Here's how you can download the source code.

```
git clone https://github.com/katewolffe/katewolffe.github.io.git
```

Your name lives in a file called `_config.yml`. Open it. You'll see a line with starting with `title:`. Change that line to be whatever you want, it'll appear in the sidebar to the left, then save and exit.

Run your website locally to see what it looks like with your change:
```
bundle exec jekyll serve
```

You should see:
```
Configuration file: /Users/maxwolffe/Workspace/katewolffe.github.io/_config.yml
Configuration file: /Users/maxwolffe/Workspace/katewolffe.github.io/_config.yml
  Source: /Users/maxwolffe/Workspace/katewolffe.github.io
    Destination: /Users/maxwolffe/Workspace/katewolffe.github.io/_site
      Incremental build: disabled. Enable with --incremental
        Generating...
        done in 0.533 seconds.
        Auto-regeneration: enabled for '/Users/maxwolffe/Workspace/katewolffe.github.io'
        Configuration file: /Users/maxwolffe/Workspace/katewolffe.github.io/_config.yml
        Server address: http://127.0.0.1:4000//
        Server running... press ctrl-c to stop.
```

Go to chrome and enter `http://127.0.0.1:4000` into the address. You should see this site (but with your changes.) It's running on your computer!

If you are happy with it, then "save" it by putting the following two commands into your command line (terminal).

```
git add .
```
Then
```
git commit -am "Changing the title of my website, this is a comment and can be anything."
```

Finally, upload it to Github with this command:

```
git push origin master
```

That's it, give it a shot yourself (you can't break anything), and I'm here for you if you need a hand.

### Writing new posts.

This is a sample blog entry. These all live in the `_posts` directory, and you can add your own! You need to follow the format I've used when naming the file `year-month-day-title.md`. You'll also notice that the formatting is a little strange. It's written using a standard called Markdown. It's actually very simple, and a great skill to learn. Here's a quick tutorial to get you started :).

Once you've written your first post, follow the steps that you did above to commit and push it to Github, and it'll show up alongside this post.

### The Sky is the Limit

This is your site. Let me know what you want to change about it. In case you can't tell, it currently looks a lot like [maxwolffe.com](http://www.maxwolffe.com), which is a great site, and will be changing soon, but isn't YOUR site. Do you want the color to be different? Do you want to use a totally different theme? Do you want a "Contact me" form? Do you want a DISQUS forum so people can comment on your blog posts? Do you want the nav bar to be on the right? I'm here to help you make it yours, let me know what you want different right now, and I'll fix it. When you're back we can sit down and make it EXACTLY what you want together.

Love always,

Max Wolffe