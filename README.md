# rss-icon

an rss icon in pure CSS

I wanted to add an RSS button to my wobsite.

There's a lot of cool stuff you can do with modern CSS, so whenever I have to choose between adding a static image and constructing something with CSS, I prefer CSS.

These things can be really time consuming, though, and since I'm really lazy I usually start by looking for other people's work which I can rip off.

I found [this codepen](http://codepen.io/dazulu/pen/bBfDm) which did what I wanted.

Unfortunately, it used some non-prefixed styles that would interfere with pretty much any stylesheet that you added it to.

I decided to refactor it all into LESS, and pull some values out into variables so that it would be easier to reconfigure.

## Usage

`rss.less` provides a single mixin (`.m-rss-icon`) that you can use in your less stylesheets.

It takes three arguments which all have somewhat sane defaults.

1. size
  - default: `50px`
  - ideally in pixels, but feel free to experiment
2. background-color
  - default: `#ffbb52` (the usual orange rss background)
3. color
  - default: `#fff` (white)

You probably want to use this mixin to target `a` (anchor) elements.
See `example.less` for an example.

## Compiling


```bash
# You'll need a less compiler.

# if you don't have one
sudo npm i -g less

# now compile it
lessc example.less
```

## Shoutouts

Thanks to [Adrian Payne](http://codepen.io/dazulu/) (blog at [Frontend Irish](https://frontend.irish/)) for the awesome codepen that got me started.
