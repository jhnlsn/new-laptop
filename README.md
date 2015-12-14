# new-laptop
Stuff that I do when I get a new laptop, usually a macbook pro or similar

So many things to do when you get a new laptop and I just want to remember them all in one place without having to go somewhere else.  I'm pretty random so these things are in no particular order.  All steps outlined are for a MB Pro.  If you develop for the web on anything else, well I'm sorry please talk to your respective manager and let him know you will be quitting soon.

Took inspiration from a couple of other places. https://github.com/nicolashery/mac-dev-setup

# All the stuff

I'm so indecisive when it comes to writing stuff down and then I get all hung up on the formatting instead of getting the information down. `do I want to do this in a list or headlines... sigh`  I know that good content > formatting but what ever I'm a little OCD so what ever.

- [Iterm](#iterm)
- [Homebrew](#homebrew)
- [oh my zsh](oh-my-zsh)
- [nvm](#nvm)
- [Git](#git)
- [Webstorm](#webstorm)
- [Atom](#atom)
- [Parallels](#parallels)
- [Spotify](#spotify)
- [1password](#1password)
- [Docker](#docker)

## [Iterm](https://www.iterm2.com)

Because terminal is too boring.  Not a whole lot more to say here and yes I'm that opinionated.

## [Homebrew](http://brew.sh)

You could use another package manager like macports, but just don't.  You're probably also thinking to yourself, why is this guy not writing up how to install this stuff here?  Well, thanks for thinking about it!  Since my voice is in your head for the time being, let me just sing the song of my people. Weird huh?  Yea i'm a bit weird, but you are reading this after all :p

Anyways, i'm not going to tell you how to install this thing or most other things unless there is some weird quirks that I found while installing.  Ok bye.

## [Oh My Zsh](http://ohmyz.sh)

Spending most of the day in the terminal and at the end of the day my brain can only hold so many command shortcuts, which is why this is a must!  It's only as good as the plugins you have activated.  Go to your `~/.zshrc` file and edit the plugins list to add the stuff you use the most.

### Plugins

My current config.

```
plugins=(git docker docker-compose node npm nvm gitignore httpie)
```

## [NVM](https://github.com/creationix/nvm)

Like RVM, but for node.  Enables you to install multiple versions of node and switch between them.  Very useful for development.  Also encapsulates your global modules, which is helpful sometimes and a pain in the ass others.

## Git

Yay we have homebrew so this is easy!

```
brew install git
```

## [Webstorm](https://www.jetbrains.com/webstorm/)

As of this writing, [Jetbrians](https://www.jetbrains.com) just redid their website.  I guess they wanted to get all fancy and actually do care about formatting lol.  I write a lot of javascript so this is usually what I need.

## [Atom](https://atom.io)

Great for general text editing and other simple stuff when you don't need a whole lot of other cruft that goes along with jetbrains IDE stuff.  Currently writing this README in atom :)

## [Parallels](http://www.parallels.com)

You know what to do.  $Buy it$.  Plus interestingly, their website is not https.

## [Spotify](https://www.spotify.com/)

if you don't listen to music while you code, then I don't know what to tell you.

## [1password](https://agilebits.com/onepassword)

I don't care what sort of password manager you use, but use one kids.  Don't use drugs and the same password on all of your websites!  Pick one or the other or something like that!

## [Docker](https://www.docker.com)

I have only recently discovered the power of docker.  It plays an important role for a macbook because you don't have to litter up your brand new MB Pro with Mysql, Postgres or Elasticsearch server infrastructure and wonder what's going on.  Not to mention the install is going to be different on a MBPro VS your actual dev/production environment.  With docker this all changes.  Now you can run your respective infrastructure in a docker container as needed.  Most images are already available and setup.

### Setup

If you are not familiar with docker then I would suggest going through the getting started guide on the [docker](https://docker.com) website.  Otherwise I'm going to assume you already know why docker is a good thing and go from there.

First thing you are going to need to do is install the docker toolbox.  This is going to give you all the fun stuff, including VirtualBox.  I dropped VirtualBox for Parallels at the recommendation of [inadarei](https://github.com/inadarei).  If you don't want to use parallels then you should be all set!  Move on to other sections that outline the specifics to install the docker container.

**Read below if you have a license for parallels**

After installing docker toolbox, you are going to want to deactivate the VirtualBox machine.  To do this you will first need to figure out its name.

`docker-machine ls`

```
NAME      ACTIVE   DRIVER       STATE     URL                      SWARM   ERRORS
default   -        virtualbox   Running
```

Go ahead and kill this thing `docker-machine kill default`.  Now that the virtualbox image is dead, we can move on to installing the parallels driver.
