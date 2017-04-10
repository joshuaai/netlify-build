# Jekyll 3.0 on Netlify

Install `jekyll` if you don't already have it:
```bash
gem install jekyll
```

Create the new project and use the `jekyll` server to display it on the browser:
```bash
jekyll new netlify-build

cd netlify-build

jekyll serve
```
The project gets loaded on `localhost:4000`.

**------If you don't have Rails installed already------**
To make the site better compatible with *Netlify*, run the following:
```bash
bundle init
```
This will create the `Gemfile` in the jekyll directory. In the `Gemfile` replace:
```ruby
# gem ruby
```
with
```ruby
gem jekyll
```
Run `bundle install` to install the gem.
This file will ensure that Netlify always uses the same version of Jekyll that you used to build your site, thus avoiding any nasty surprises.
**-----------------------------------------------------**

## Creating the Github Repo
Create a new repository on GitHub with the name `netlify-build`. To avoid errors, *do not* initialize the new repository with `README`, `license`, or `gitignore` files. You can add these files after your project has been pushed to GitHub.

Run the bash commands:
```bash
echo "# netlify-build" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/joshuaai/netlify-build.git
git push -u origin master
```


