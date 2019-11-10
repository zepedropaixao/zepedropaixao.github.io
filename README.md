# TODO

Execute this command to run page locally

```
gem install jekyll bundler
bundle install
bundle exec jekyll serve
```


# If it fails to install:

## Install rbenv via brew
``` 
brew install rbenv ruby-build
```

## Add rbenv to bash so that it loads every time you open a terminal
``` 
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile
``` 

## Install Ruby through rbenv and set as default
``` 
rbenv install 2.6.3
rbenv global 2.6.3
``` 

## Install Jekyll
``` 
gem install bundler jekyll
``` 
