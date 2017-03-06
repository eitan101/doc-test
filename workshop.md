---
permalink: workshop.html
---

# Workshop Flow

## Prerequiesites 
* docker
* docker pull jekyll/jekyll

## Github Pages
1. Create a repo in github.com with Readme.
2. Settings -> Github Pages -> 
   Select master branch
   Select Theme;
   Navigate to the link in the github-pages section
3. Create a file
```markdown
---
layout: default
---
Your markdown here
```
navigate to the page

## Open API Spec
1. Read the [spec](https://github.com/OAI/OpenAPI-Specification/blob/3.0.0-rc0/versions/3.0.md)
2. See the [editor](http://editor.swagger.io/#!/)
3. See [redoc](https://github.com/Rebilly/ReDoc).
4. Add spec file with the example in the editor to your repo. Call it spec.yaml
5. Add redoc.html file as folows:
```html
```
6. Task: edit the spec yaml to reflect csds api, or any other lp rest-api.

## Jekyll
1. Pick a theme from [here](http://jekyllthemes.org/)
2. Fork the theme, for example [this](http://jekyllthemes.org/themes/vision-casper-theme/).
3. Clone it.
4. Run
```sh
docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll \
  -it -p 127.0.0.1:4000:4000 jekyll/jekyll jekyll serve
```

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



