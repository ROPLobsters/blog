# rop-lobsters-site

This repo maintains the blog for ROP-Lobsters podcast!

> NOTE: Hugo version is pinned in `.github/workflows/.gh-pages.yml` workflow.
Locally deploy test before up-leveling.

### Development

Installation: https://gohugo.io/installation/

This repo is powered by:
- Hugo Framework - [link](https://gohugo.io/about/)
- PaperMod Theme - [link](https://github.com/adityatelange/hugo-PaperMod/wiki/)
- Castanet Theme - [link](https://github.com/mattstratton/castanet)

#### Updating PaperMod theme

We consume the main branch of PaperMod Theme - [link](https://github.com/adityatelange/hugo-PaperMod/wiki/). In order to pull the latest version of the theme follow:

```
# Init and realize that there are submodules
git submodule update --init
# Pull the latest commit from remote
git submodule update --remote --merge
```

Then it should show under diff, commit it normally like any other change.

#### Local Dev
To spin up a local web-server, run the command from **root of this project**:
```
hugo server -D
```
Then you should be able to see your website at http://localhost:1313 . Note that
the command monitors your local changes and updates the website rendering in
realtime.

#### Deployment
- Switch to a new branch  - `git checkout -b <new_branch_name>`
- Commit your changes
- Send a PR

Or just commit your changes to `main` branch, IDK `\_O_/`. The github action
will pickup your changes and deploy to live.

### Code org
- `archetypes/*` - Templates for posts
- `content/*` -  All the good stuff, follow good naming structure since the URL
path is derived from the folder structure in here
- `layouts/*` - Allows us to do custom addons to the theme and more
- `static/*` - Contains static content which we just want to be copied over like
images, resources etc
- `themes/*` - Don't worry about it for now, dark magic
- `config.yml` - Configuration for the project and themes, refer
[theme guidelines](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation)
on things we could add here.
