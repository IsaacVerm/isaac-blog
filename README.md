# README

## Install Hugo

On [Mac OS](https://gohugo.io/getting-started/quick-start/):

```
brew install hugo
```

## Create blog

```
hugo new site blog
```

## Create post

```
hugo new posts/blablabla.md
```
Post will be added to `/content/posts` folder.

## Start server

If you just use `new posts` the post created will have draft status set to true. This means the post will not be published. We want to see what the post looks like so we have to override this default behaviour. Hence the `-D` argument for the server.

```
hugo server -D
```

## Theme

Uses default Ananke theme.