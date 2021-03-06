# :green_book: ntbk

*ntbk* is a simple command-line journaling tool written in Node.js.

## Installation

To install *ntbk* using npm:

```
npm install -g ntbk
```

## Usage

Type `ntbk` into your shell window followed by a message:

```
> ntbk 11-month-old stood up today for the first time
```

then hit enter to have the entry added to your designated notebook.

Alternatively, you can type `ntbk` and hit return and then type your message. When you're ready to save your entry, hit return again.

### Options

#### -l, --list [n]

You can see all your entries by using the `--list` option:

```
> ntbk --list
```

You can also pass a number to the `--list` option and it will return a subset of your entries. For example if you passed 2 it will return the last two *ntbk* entries.

```
> ntbk -l 2
```

The above uses the shorthand version `-l` of the `--list` option.

#### -t, --tag \[tag\]

As you write entries in *ntbk* you might want to group similar entries together. You can do this by using *tags*.

*ntbk* supports Twitter like hashtag syntax.

```
I really think pizza is the best! #food
```

The syntax is a word that describes your entry with a hash (#) symbol prepended. Tags can be used anywhere within your entry.

When using tags while writing your entry, you might have to escape them using the backslash (\\) character.

```
> ntbk Implemented tags in ntbk today \#dev
```

To list all *ntbk* entries containing a tag, you can use the `--tag` option:

```
> ntbk --tag food
```

As you can see in the example above, the tag option doesn't need to have the hashtag symbol prefixed when passing it a parameter.

You can also get a list of all existing tags in your notebook. Simply use the `--tag` option without passing in a tag as a parameter:

```
> ntbk --tag
```

The shorthand version of `--tag` is `-t`.

#### -m, --moments \[value\_unit\]

Like a time machine, the `--moments` option allows you to relive your past entries from a year go.

```
> ntbk --moments
```

If you didn't write any entries a year ago from your current day, no problem, *ntbk* will retrieve a random moment from your entries.

The `--moments` option also allows you to pass in several time units to retrieve moments in time.

Let's say instead of a year, I wanted to relive my moments from last month, I could do this:

```
> ntbk --moments 1m
```

As you can see the syntax goes, numerical value paired with a single character unit. The units of time that `--moments` recognizes are:

```
d - day
m - month
y - year
```

The shorthand version of `--moments` is `-m`.

#### --count, -c \[emojify\]

See how many entries you've got in your notebook with `--count`.

```
> ntbk --count
```

## Changelog

### v0.5.3 / 2017-07-18

Added information on how to hack on *ntbk* from local machine.

### v0.5.2 / 2016-06-29

The `--tag` option can now [list existing tags](https://github.com/michaellee/ntbk/tree/develop#-t---tag-tag) from your journal. Run `ntbk --tag` without passing a tag and it'll list all your tags.

### v0.5.1 / 2016-06-28

Fixed a bug with `--moments` where the default entry is a year from today.

### v0.5.0 / 2016-06-23

See how many entries you've captured in your notebook with `--count`.

[See all releases](https://github.com/michaellee/ntbk/releases)

## Credit

*ntbk* was inspired by the Python journaling app, [jrnl](https://github.com/maebert/jrnl).

## Make it better

Help make *ntbk* better. If you're handy with some JavaScript and/or Node.js, feel free to create a pull-request. You could also [create a new issue](https://github.com/michaellee/ntbk/issues/new) on GitHub. If you have any questions feel free to shoot me a tweet [@michaelsoolee](https://twitter.com/michaelsoolee).

To hack on *ntbk* on your local machine, first clone the repo, then from within your local copy, type `npm link`. This will make a symlink to your local copy.

## License

[MIT](https://github.com/michaellee/ntbk/blob/master/LICENSE) &copy; [Michael Lee](https://michaelsoolee.com)

[newsletter]: http://eepurl.com/b67A_1
