## Introduction

This is a *Visual Studio Code* extension to help you write user snippets quickly. See below demonstration.

![Feature demonstration](https://raw.githubusercontent.com/yangshuairocks/MySnippetMaker/master/images/mysnippetmaker_intro.gif)

## Features

- Escape snippet special characters
- Snippet tab stop helper
- Able to reset tab stop counter
- Provide an intuitive way to create a snippet
- The extension will help to translate the user-friendly snippet syntax to Visual Studio Code native snippet

## How to use

After you installed this extension, you have a snippet to help you to create other snippets. <kbd>ctrl</kbd> + <kbd>n</kbd> create a new file and type `skel`, press <kbd>tab</kbd>, you will have a snippet skeleton. Press <kbd>tab</kbd> to fill the *name*, *scope*, *prefix* and *body* of your snippet. Below is an example:

```
Name: keyboard HTML markup - describing shortcuts on web
Prefix: kkk
----------------------------------------
<kbd>ctrl</kbd>
```

Here I didn't specify the *scope* for this snippet, so it is a global snippet and will be available for all file types.

Optionally, I can select the text `ctrl` between `<kbd>` and `</kbd>` and press <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>x</kbd>. Now the text `ctrl` will be automatically changed to `${10:ctrl}`. Next time when you press <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>x</kbd> again, you will get a tab stop with counter 20 like this `${20:some_text}`. The idea is that you can easily create tab stops with an increment of 10 and this makes it easy for you to modify you snippet later, for example add a new tab stop `${15:}` somewhere between `${10:}` and `${20:}`. This will be very hard if you are using continous tab stop counters. 

Another feature this extension provides is escape special snippet characters. Select the text you are going to escape and manually invoke this feature by pressing <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> and type `edde`. Find the command and press <kbd>enter</kbd>.

When you finished editing the snippet, press <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>z</kbd>, a snippet file will be created in the snippets folder.

Note that, if the shortcuts do not work, you can always press <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> and type `edde` to call the commands provided by this extension manually. You can also specify your own shortcuts for them.

## Cool features

1. You can use multiple prefixes for the same snippet and this extension will help you to create multiple snippet files. For example, if you have the following template:

```
Name: import a module
Scope: python
Prefix: req, imp
----------------------------------------
require ${10:sys}
```

After you press <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>z</kbd> to create the actual snippets, the following two snippets files will be created.

```
python.[imp - import a module].code-snippets
python.[req - import a module].code-snippets
```

2. This extension will correctly create valid file names for you. Invalid file name characters will be removed and continuous white spaces will be replaced with just a single space character.

## Installation

![How to install](https://raw.githubusercontent.com/yangshuairocks/MySnippetMaker/master/images/mysnippetmaker_install.gif)

## License

Copyright © 2018 Yang Shuai <yangshuai at gmail.com>

This work is free. You can redistribute it and/or modify it under the terms of the [wtfpl](http://www.wtfpl.net), Version 2, as published by Sam Hocevar. See the [COPYING](https://github.com/yangshuairocks/MySnippetMaker/blob/master/COPYING) file for more details.