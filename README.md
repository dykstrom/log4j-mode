# log4j-mode

<div style="text-align: left">

[![MELPA](https://melpa.org/packages/log4j-mode-badge.svg)](https://melpa.org/#/log4j-mode)
[![MELPA Stable](https://stable.melpa.org/packages/log4j-mode-badge.svg)](https://stable.melpa.org/#/log4j-mode)
[![Open Issues](https://img.shields.io/github/issues/dykstrom/log4j-mode)](https://github.com/dykstrom/log4j-mode/issues)
![License](https://img.shields.io/github/license/dykstrom/log4j-mode)

</div>

Package log4j-mode is a major mode for viewing log files in Emacs. It can
be used to view any text-based log file, even though the name refers to a
specific logging package. log4j-mode provides syntax highlighting,
filtering, and source code browsing for log files.

There are many applications that can be used to view log files, but using
log4j-mode allows you to do it without leaving Emacs.


## Features


### Syntax highlighting

log4j-mode uses customizable regexps with keywords such as DEBUG and
ERROR to syntax highlight log records. Different faces are used for
different log levels. The user can customize both the regexps, and the
faces that are used for syntax highlighting.


### Filtering

log4j-mode can filter a log file buffer using keywords specified by the
user, creating a new buffer that contains only matching log records. When
the source buffer is auto reverted, the filter buffer will be updated
too.


### Source code browsing

Source code browsing for Java code is provided using
[jtags](http://jtags.sourceforge.net)&mdash;an Emacs package for editing 
and browsing Java source code. It is possible to jump from a log file to 
a point in the source code where a certain log record was generated.

If you are not using jtags, or if you are not working with Java, you can 
still use the built-in tags lookup feature. Type M-. to run the find-tag 
command in the _etags_ package.


## Usage

For information on using log4-mode, please see the commentary section in
file [log4j-mode.el](src/log4j-mode.el).


## Installation

The recommended way to install log4j-mode is from [MELPA](https://melpa.org).

To install manually, place log4j-mode.el in your load-path, and add the
following lines of code to your init file:

```elisp
(autoload 'log4j-mode "log4j-mode" "Major mode for viewing log files." t)
(add-to-list 'auto-mode-alist '("\\.log\\'" . log4j-mode))
```
