+++
title = 'I write code sometimes.'
date = 2021-09-01
+++

(This is an adaptation of a similar page on the previous version of this website.)

At any given time, I am up to my eyeballs in projects.  What follows is an incomplete list of software development projects.  More project information can be found in my [Fossil Record](http://fossrec.com/u/apotheon), though that too provides an incomplete picture.

### Original Software

These are cases where I have created a new software project from scratch and developed it to a point where it may be worth releasing to the world.

#### C Utilities

##### Q[ueuer]

I wrote a shell script as a way to manage a day's worth of things to do, and called it Queuer, or Q for short.  It manages a mutant "queue", with features of a ring buffer, and its design implies a particular workflow that helps ensure things actually get done.  In 2018, after a few years of using it to some good effect, I rewrote it in C.  It might need more rewriting.

* [Project Homepage](https://fossrec.com/u/apotheon/q)

#### Ruby Gems

##### Droll

In the first half of 2012, I published a Ruby gem called "droll" (for "die roll") that I created for my own use as a roleplaying gamer.  It is a library providing some sophisticated dice rolling simulation functionality, allowing for a number of complex operations in generating (pseudo-)random die roll results including "exploding" dice, selection of high or low values, counting dice that meet a threshold requirement, and other nifty capabilities that are familiar to many roleplaying gamers.  Despite all that, it is not the most complex gem available by any stretch of the imagination, but I think it is a pretty decent effort.

In addition to the library itself, which provides the Droll class, the gem also comes with two user interfaces -- a command line dice rolling utility and an IRC dicebot.  I find the results adequate.

In addition to roleplaying game uses, the library could also quite easily be used in other contexts where dice (or similar random number generation) would be appropriate, such as a digital craps game.  I think RPGs represent the most sophisticated, purely entertainment-oriented use of dice I have encountered, however, so as long as I focus on satisfying the needs of roleplaying gamers I think I should be able to serve pretty much any needs of other, related users.

* [RubyGems Page](https://rubygems.org/gems/droll)
* [Project Homepage](https://fossrec.com/u/apotheon/droll)

<!-- * [Bitbucket Repository](https://bitbucket.org/apotheon/droll) -->

##### CharsetMove

As of July 2012, I published my second Ruby gem, called "charset_move".  It has a nominal library providing a CharsetMove class, but it's mostly useful just for the `cmv` command line utility interface that is installed with it.

The `cmv` utility "moves" a file, translating its name from one specified encoding to another.  In short, it is a filename transcoder.  It was inspired by a friend's search for a simple way to transcode filenames.  It takes about the simplest approach that came to mind at the time.

* [RubyGems Page](https://rubygems.org/gems/charset_move)
* [Project Homepage](https://fossrec.com/u/apotheon/cmv)

<!-- * [Bitbucket Repository](https://bitbucket.org/apotheon/CharsetMove) -->

##### RedRug

As of September 2012, I published my third Ruby gem, called "redrug".  It is a simplified interface to some of the functionality of [Redcarpet](https://github.com/vmg/redcarpet) (a Markdown parser based on [Sundown](https://github.com/vmg/sundown), which was based on [upskirt](http://fossil.instinctive.eu/libsoldout/index)), for common use cases.

I created it because it took me a grand total of one use of Redcarpet to decide I was tired of the overly verbose syntax required to get Redcarpet to do the stuff I wanted it to do.  I understand why Redcarpet works the way it does; it is, relative to RedRug, a low-level library providing significant flexibility and power.  For my purposes, I generally do not need all of that, so I wrote a wrapper library to simplify the interface.

Within a day after being published, this library had already become my most popular Ruby gem, as measured by the "downloads" numbers on [rubygems.org](http://rubygems.org).  In fact, it had more downloads within one day than the other two gems combined.

* [RubyGems Page](https://rubygems.org/gems/redrug)
* [Project Homepage](https://fossrec.com/u/apotheon/redrug)
* [GitHub Mirror](https://github.com/apotheon/redrug)

##### Versionize

As of October 2012, I published my fourth Ruby gem, called "versionize".  It is just a dead-simple way to manage version numbers in Ruby software, which I created because I wanted more than just a hardcoded string and accessor in my Ruby gems.  There is not a whole lot to it, but it serves my needs, and after the first month of availability it seemed like it might serve the needs of about 130 other people (the download numbers at rubygems.org at the time) as well.

* [RubyGems Homepage](https://rubygems.org/gems/versionize)
* [Project Homepage](https://fossrec.com/u/apotheon/versionize)

<!-- * [Bitbucket Repository](https://bitbucket.org/apotheon/versionize) -->

##### CreepCheck

As of April 2015, I published my fifth Ruby gem, called "creepcheck".  It is an "April Fool's Project", in that each April Fool's Day for a few years I made updates to this joke-project, and I only updated it for April Fool's Day.

* [RubyGems Homepage](https://rubygems.org/gems/creepcheck)
* [Project Homepage](https://fossrec.com/u/apotheon/creepcheck)

##### FossGit

As of December 2016, I published my sixth Ruby gem, called "fossgit".  It is a command line utility that makes the process of mirroring Fossil SCM repositories in Git repositories more convenient.  This includes pushing Git mirror updates to GitHub and GitLab, if you have a GitHub and/or GitLab repository for your Git mirror.  It wraps the command line interfaces of both Fossil and Git to achieve these ends.  I made plans to extract a library from the command line tool, which the utility would then wrap to create its command line interface, and to later merge that library into a larger project providing a Fossil API in Ruby, with FossGit itself becoming a consumer of that API.  Unfortunately, some updates to Fossil introduced breaking changes in the CLI, and this project is currently, effectively, dead.  I will likely rewrite it to wrap the new command line interface of Fossil SCM or just replace it with a tool that works altogether differently.  If you (for some reason) use an old enough Fossil version, this may still be useful; otherwise, skip it.

* [RubyGems Homepage](https://rubygems.org/gems/fossgit)
* [Project Homepage](https://fossrec.com/u/apotheon/fossgit)
* [GitHub Mirror](https://github.com/apotheon/fossgit)


### Software Contributions

These are cases where I have contributed my time to working on software projects run by other people.  It is by no means comprehensive.  It's very easy to forget about even significant contributions that I could add here when it's not my own project, and if it has been too long since I've had any association with the project I might remove it from the list some day.  At present, it is woefully out of date.

#### C Libraries

I became a significant contributor to a behavior driven development (BDD) library for C called [bdd-for-c](https://github.com/grassator/bdd-for-c), when I started using it for my Queuer project.

#### FreeBSD Ports

Years ago, I started maintaining one port for FreeBSD, [xsel-conrad](http://www.freshports.org/x11/xsel-conrad/).  From the port description:

> XSel is a command-line program for getting and setting the contents of the X selection. Normally this is only accessible by manually highlighting information and pasting it with the middle mouse button.
>
> This port is similar to x11/xsel, but with different CLI syntax and a bit more functionality. It is a lot more popular, too.
>
> WWW: [http://www.vergenet.net/~conrad/software/xsel/](http://www.vergenet.net/~conrad/software/xsel/)

I picked up support for the port because I use the heck out of this utility, it was previously unmaintained, and the port needed a minor Makefile fix-up or two.  All things considered, it's a pretty minor project, given how slowly a tool like this needs to change.  I didn't even have to do anything to get it to compile with Clang.
