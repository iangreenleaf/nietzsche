# Nietzsche for you #

Put Nietzsche in your fortunes.

![Sample screenshot](./screenshot.png)

This project collects aphorisms from various works by Friedrich Nietzsche, and makes them available in a machine-readable format compatible with UNIX `fortune` utilities.

## Usage ##

The simplest way to use this is:

    fortune this_project/fortune

You might want to limit the length of texts that will be chosen.
This is my preferred command:

    fortune -s -n 400 this_project/fortune

And you'll probably want to decorate your fortune as well.
I like the `cowsay` utility:

    cowsay $(fortune -s -n 400 this_project/fortune)

## Developing ##

Got more aphorisms to contribute?
Please do!

### Building the data files ###

The source files that you should be editing are located in `./src`.
Files in `./fortune` are machine-generated.

If you have added or modified text, re-flow it to match the standard line width:

    ./bin/reflow src/*

Any time the contents change, you'll want to re-generate the data files:

    ./bin/build

## License ##

All works in `src` were originally made available under public domain.
Some of the works were graciously provided by [Project Gutenberg](http://www.gutenberg.org).

All contents of this project are made available under the WTFPL.
See [COPYING](./COPYING) for more information.
