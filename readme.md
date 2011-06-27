# Enscript Extras

The file `enscript.st` is a replacement for the file which ships with enscript/states of the same name. This version uses CSS for syntax highlighting when exporting to XHTML, and includes markers for the beginning and ends of the CSS styles. It also includes a new, unstable php highlighter.

I made these modifications so the highlighting output could be more easily included in web application workflows.

To use, copy `enscript.st` to `/usr/share/enscript/enscript.st`, and run enscript on your source file (let's say `/tmp/foo.m`, written in Objective-C) like so:

```sh
enscript -q -p - --pretty-print --language=xhtml --color /tmp/foo.m
```

Or, you could explicitly specify Objective-C with:

```sh
enscript -q -p - --pretty-print=objc --language=xhtml --color /tmp/foo.m
```

Otherwise enscript will try to make an educated guess.

To see which languages enscript supports pretty printing, run:

```sh
enscript --help-pretty-print
```

For easy parsing of the output, I surround the CSS styles with:

```html
<!--begin-style-->
```

and

```html
<!--end-style-->
```

The highlighted code is already easily parsed because it's surrounded by pre 
tags.

For copypright information, see `COPYING.txt`.

# Contact

[Andrew Wooster](http://andrewwooster.com/)

[GNU Enscript](http://www.markkurossi.com/genscript/)
