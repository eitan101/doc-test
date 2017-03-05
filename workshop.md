---
permalink: workshop.html
---

# flow

## Prerequiesites 
docker pull jekyll/jekyll

## create repo
add github pages minimal

redoc copy index.html
swagger.editor copy yaml
edit index.html

jekyll fork space-jekyll-template
switch gh-pages.
edit
commit
see

clone

```sh
docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll \
  -it -p 127.0.0.1:4000:4000 jekyll/jekyll jekyll serve
```

dev-hub

fork jekyll
build locally

docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll \
  -it -p 127.0.0.1:4005:4005 jekyll/jekyll bash
bundle install
bundle exec jekyll serve

add md
add redoc page



