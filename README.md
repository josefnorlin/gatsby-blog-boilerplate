# gatsby-blog-boilerplate

Get fast up and running with a blog boilerplate using static page generator using Gatsby (a blazing-fast static site generator for React) and a CMS with Contentful hosted by Netlify.
 
## Contribution

This project is based on the contentful-starter project. Read more about it here: https://github.com/contentful-userland/about.

## Requirements

- Contentful account, get one for free here: https://www.contentful.com/sign-up/.

- Netlify account, get one for free here: https://app.netlify.com/signup.

## Getting started

1) First make sure you have npm installed on your machine
- Windows check here: http://blog.teamtreehouse.com/install-node-js-npm-windows
- Mac:
    a) Install Homebrew
    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

    b) Install npm
    brew install node
- Linux: 
    Run this command in the terminal (Ctrl + Alt + T)
    sudo apt update && sudo apt install nodejs

2) Install the Gatsby CLI
npm install --global gatsby-cli

3) Create a new Gatsby project using this github rep
gatsby new contentful-starter https://github.com/josefnorlin/gatsby-blog-boilerplate

4) When that is up and running, go to that directory and the following command
gatsby new gatsby-blog-boilerplate https://github.com/josefnorlin/gatsby-blog-boilerplate


RUN LOCALLY:
1) Go to your folder (cd [folder location])

2) (only the first time) npm run setup

3) Run: npm run dev


DEPLOY:
1) (only the first time) First make sure you've installed netlifyctl by running:
- Windows:
    1) Install scoop:
    Make sure Powershell 3 (or later) and .NET Framework 4.5 (or later) are installed. Then run:
    
    iex (new-object net.webclient).downloadstring('https://get.scoop.sh')

    2) Use scoop to add netlifyctl as a bucket:
    scoop bucket add netlifyctl https://github.com/netlify/scoop-netlifyctl
    
    3) Then install it by:
    scoop install netlifyctl

- Mac:
    1) Add netlify tap to brew:
        brew tap netlify/netlifyctl
    
    2) Install it running:
    brew install netlifyctl

- Linux:
    Follow the instructions here: https://github.com/netlify/netlifyctl


2) (only the first time) Go to your folder (cd [folder location])

4) (only the first time) Login to:
netlifyctl login

3) Build the website by running:
npm run build

5) Deploy it:
npm run build && netlifyctl deploy -b public


### Set up of the needed content model and create a configuration file

This project comes with a Contentful setup command `npm run setup`.

![Command line dialog of the npm run setup command](https://rawgit.com/contentful-userland/gatsby-contentful-starter/master/setup.jpg "Command line dialog of the npm run setup command")

This command will ask you for a space ID, and access tokens for the Contentful Management and Delivery API and then import the needed content model into the space you define and write a config file (`./contentful.json`).

`npm run setup` automates that for you but if you want to do it yourself rename `.contentful.json.sample` to `.contentful.json` and add your configuration in this file.

## Crucial Commands

### `npm run cleanup-repository`

Removes all dependencies, scripts and data from the installation script.

## Other resources

- Tutorial video series ["Building a blazing fast website with GatsbyJS and Contentful"](https://www.youtube.com/watch?v=Ek4o40w1tH4&list=PL8KiuH6vpACV-F7jXribe4YveGBhBeG9A) by @Khaledgarbaya
