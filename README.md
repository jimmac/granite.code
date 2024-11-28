Granite.code website
==============

To set up jekyll locally on Fedora:

1) Set up Toolbx container and clone the repo
```
toolbox create granite-website --release 41
toolbox enter granite-website
mkdir src && cd src
git clone git@github.com:jimmac/granite.code.git
cd granite.code
```

2) Set up ruby and install rvm
```
sudo dnf install -y curl gcc-c++
sudo dnf builddep -y ruby
\curl -sSL https://get.rvm.io | bash -s stable
echo "source ~/.rvm/scripts/rvm" >> $HOME/.bash_profile
source $HOME/.bash_profile
rvm install ruby-3.1.2
bundle install
bundle exec jekyll s
```

The CI should deploy the site automatically to [FIXME](#fixme).
