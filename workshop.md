---
permalink: workshop.html
---

# Workshop Flow

## Prerequiesites 
* docker
* docker pull jekyll/jekyll

## Github Pages
1. Create a repo in github.com **with Readme**.
2. Settings -> Github Pages -> 
   * Source: master branch
   * Select Theme;
   * Navigate to the link in the github-pages section
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
5. Add redoc.html file as [folows](https://raw.githubusercontent.com/eitan101/doc-test/master/kk.html).
6. Task: edit the spec yaml to reflect [csds api](https://livepersoninc.github.io/dev-hub/current/agent-domain-domain-api.html), or any other lp rest-api.

## Jekyll
1. Pick a theme from [here](http://jekyllthemes.org/)
2. Fork the theme, for example [this](http://jekyllthemes.org/themes/vision-casper-theme/).
3. Clone it.
4. Run
```sh
docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll \
  -it -p 127.0.0.1:4000:4000 jekyll/jekyll jekyll serve
```
5. Open the browser at http://0.0.0.0:4000/
6. TBD: Create a post page as follows:
```markdown
---
layout: default
---
put your content here
```
7. Refresh the browser.
6. GithubPages + Jekyll
   * Commit the changes
   * Enable github pages for the repo
   * Open the rendered site.
   
## Liveperson Developers Hub
1. Goto [dev-hub-repo](https://lpgithub.dev.lprnd.net/pages/Architecture/dev-hub-internal/).
2. Read the README.md
3. Fork the repo
4. Task 1: Add md page
5. Task 2: Add redoc page with some rest-api
   
