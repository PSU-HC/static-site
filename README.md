# Simple File Hosting

Static site built with [Hugo CLI](https://gohugo.io/getting-started/quick-start/)

*Note, file core_psu-hacking.iso is omitted for size constraints-
hosted site contains this file @ directory /static/static/*
```
# on OSX
# get hugo

brew install hugo

# clone site

git clone https://github.com/psu-hacking/static-site
cd static-site

# Compile and compress public directory

hugo
zip -r site-archive.zip public

# upload and host with sftp & ssh

sftp user@yoursite.net
> cd yoursite.net
> put site-archive.zip

# new terminal window

ssh user@yoursite.net
> unzip site-archive.zip
> cd # back to sftp root- example is using Dreamhost as remote
> mv yoursite.net/site-archive/* yoursite.net
> rm -rf yoursite.net/site-archive.zip
```

Hosting planned @ psuhacking.club.
