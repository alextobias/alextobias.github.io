# _NOTES.md
Notes to myself on using Jekyll since I will probably revisit my site infrequently.

# Commands
- looks like the intended way to build and serve locally is with `bundle exec jekyll serve`
- can use `--livereload` flag for live reload
- `bundle install` installs all gems currently in Gemfile
- to bypass bundler if you aren't using a gemfile, use `jekyll serve`.
- **It seems like I have to prepend bundle exec to any jekyll command, to run said command using the installed gems for this project. So if I say `jekyll x`, do `bundle exec jekyll x`.**
- `jekyll clean` removes all generated files.

# Toolchain
- The site is generated using Jekyll, i.e. it takes more human-friendly markdown input and generates html/css that is actually displayed
- Served using github pages, which supports Jekyll (so it does the building/generation on its end too)
- **Ruby**: **To manage my Ruby installation, I've installed `chruby` via homebrew.**
- **Gem**: Package manager for ruby. Jekyll and Bundler are installed as Ruby gems.
- **Bundler**: a gem that installs all gems in your gemfile. I guess it's like `npm install?`
- It seems like the purpose of Bundler is to ensure package consistency across devices, i.e. when serving from github pages. (The alternative being that you have to make sure the server machine has all the requisite gems already installed)
- The Bundler docs suggest the use of a `.bundle` file which is not added to source control. But I don't have one here, probably something to do w/ github pages. 

# Files & Directory Structure

## _config.yml
- Config file for settings that affect the entire blog site - the stuff here should be values that we intend to set up once and rarely edit
- *NOT* reloaded automatically under `bundle exec jekyll serve`; must restart server process

## assets/css/style.scss
- This file is for overriding the default theme css

## Gemfile & Gemfile.lock 
- `Gemfile` and `Gemfile.lock` seem to be analogous to npm's `package.json` and `package-lock.json` respectively.

## _posts
- blog-post style posts go here.

## _site
- Where the built files are located.

## _drafts
- Draft posts aren't normally shown, but can be previewed with `jekyll serve --drafts` or `jekyll build --drafts`

