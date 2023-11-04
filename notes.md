### Installation procedure

https://jekyllrb.com/docs/installation/ubuntu/

---

### To update after modifying the `_config.yml`:
```
$ bundle update
```

### To generate locally the webpage:
```
$ bundle exec jekyll serve --livereload
```

### To push only the `_site` subdirectory to the banch `gh-pages`:

Before doing this, you should push your changes to `main`.
```
$ git branch gh-pages
$ checkout gh-pages
$ bundle exec jekyll serve --livereload
$ git commit -m "Push to gh-pages"
$ git subtree push --prefix _site origin gh-pages
```
You may have to go to `Settings/Pages` on the GitHub webpage and selection `Source: Deploy from a branch` and `Branch: gh-pages /root`.