---
permalink: workshop.html
---

# Workshop Flow
1. Github Pages
  * Free Hosting
  * Nice Templates
  * Markdown Renderer
  * Documentation Automation
2. Open API Spec
  * Define You API in Yaml
  * Link to your JsonSchema
  * Generate Documentation
  * Generate SDKs & Mocks
3. Redoc
  * The Best API Renderer
  * Supports OpenAPI Spec
4. Jekyll
  * Build a site in a minutes
  * Add markdown content
5. LivePerson [Developers Hub](https://livepersoninc.github.io/dev-hub/)

## Prerequiesites 
* docker
* docker pull jekyll/jekyll

## Github Pages
1. Create a repo in github.com **with Readme**.
2. Settings -> Github Pages -> 
   * Source: master branch
   * Select Theme;
   * Navigate to the link in the github-pages section
3. Create a file called file.md
```markdown
---
layout: default
---
Your markdown here
```
navigate to the github pages with path /file.html.
4. Create a file called html.html:
```
\<h1\>hello world\<h1\>
```
navigate to the github pages with path /html.html.
4. Task: Upload your favorite javadoc to the repo.


## Open API Spec
1. Read the [spec](https://github.com/OAI/OpenAPI-Specification/blob/3.0.0-rc0/versions/3.0.md)
2. See the [editor](http://editor.swagger.io/#!/)
3. See [redoc](https://github.com/Rebilly/ReDoc).
4. Add spec file with the example in the editor to your repo. Call it spec.yaml
5. Add redoc.html file as [folows](https://raw.githubusercontent.com/eitan101/doc-test/master/kk.html).
6. Task: edit the spec yaml to reflect [csds api](https://livepersoninc.github.io/dev-hub/current/agent-domain-domain-api.html), or any other lp rest-api.

## Jekyll
1. Pick a theme from [here](http://jekyllthemes.org/)
2. Fork the theme, for example [this](https://github.com/mmistakes/so-simple-theme).
3. Clone it.
5. Change the title in the _config.yaml:
```yaml
title: Liveperson Tech Leader Forum
```
4. Run
```sh
docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll \
  -it -p 127.0.0.1:4000:4000 jekyll/jekyll bash
# inside the containter run
jekyll serve
```
6. Open the browser at [http://0.0.0.0:4000/](http://0.0.0.0:4000/)
6. Create a new file in the _post/blog directory called ``2017-03-07-hello-all.md``

```markdown
---
layout: post
title: "Hello my World"
modified:
categories: blog
excerpt:
tags: []
image:
  feature:
date: 2014-08-08T15:39:55-04:00
modified: 2016-06-01T14:19:19-04:00
---

You'll find this post in your `_posts` directory - edit this post and re-build (or run with the `-w` switch) to see your changes!
To add new posts, simply add a file in the `_posts` directory that follows the convention: YYYY-MM-DD-name-of-post.ext.

## Sample Heading

### Sample Heading 2

Jekyll also offers powerful support for code snippets:

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh].

[jekyll-gh]: https://github.com/jekyll/jekyll
[jekyll]:    http://jekyllrb.com
```
7. Goto [http://localhost:4000/blog/hello-all/](http://localhost:4000/blog/hello-all/)
6. GithubPages + Jekyll
  * Change the url in the _config to your github pages path:
```yml
url: https://eitan101.github.io/so-simple-theme
```
   * Commit the changes
   * Enable github pages for the master branch
   * Open the rendered site.
   
## Liveperson Developers Hub
1. Goto [dev-hub-repo](https://lpgithub.dev.lprnd.net/pages/Architecture/dev-hub-internal/).
2. Read the README.md
3. Fork the repo
4. Task 1: Add md page
5. Task 2: Add redoc page with some rest-api
