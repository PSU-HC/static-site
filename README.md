# Simple File Hosting

_ _ _
***README yet to be updated with Makerspace-specific formatting*** 
_ _ _
   
Static site built quickly with [Hugo CLI](https://gohugo.io/getting-started/quick-start/)

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
# check your remote filesystem- the idea is:
> unzip site-archive.zip
> rm -rf yoursite.net/site-archive.zip
```

[visit us](https://psuhacking.club)
