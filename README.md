ruler - a guide for terminal widths
===================================

A character ruler could be used in the status line of `tmux` or `screen` or as
part of a command line Twitter client.

An 80 column wrap is a convention, but sometimes you want an abitrary length or
the full terminal width.

An offset could be used to match width of shell prompt and script name.

With no argument `ruler` will determine the terminal environment and fit the
width, or set the length to 80 if no terminal environment exits.

In 2012 [the best tweets had under 40
characters](http://www.wired.com/2015/10/many-characters-tweet-ask-experts/),
so a ruler can remind you to be succinct.

Options
-------

    $ ruler -h
    usage: ruler [-h] [-i] [-o OFFSET] [-b BEGIN] [-l LENGTH]
    
    Make a ruler of characters; terminal width is default
    
    optional arguments:
      -h, --help            show this help message and exit
      -i, --info            Return terminal height and width; also available from
                            command `stty size`
      -o OFFSET, --offset OFFSET
                            Use spaces to offset the ruler start
      -b BEGIN, --begin BEGIN
                            Begin counting at this number
      -l LENGTH, --length LENGTH
                            Length of ruler in characters

Usage
-----

    $ ruler
    - - _ - -1- - _ - -2- - _ - -3- - _ - -4- - _ - -5- - _ - -6- - _ - -7- - _ - |8| - _ - -9- - _ - -a- - _ - -b
    
    $ ruler -i
    (75, 110)
    
    $ ruler -o 10
              - - _ - -1- - _ - -2- - _ - -3- - _ - -4- - _ - -5- - _ - -6- - _ - -7- - _ - |8| - _ - -9- - _ - -a
    
    $ ruler -l 81
    - - _ - -1- - _ - -2- - _ - -3- - _ - -4- - _ - -5- - _ - -6- - _ - -7- - _ - |8|
    
    $ ruler -o 11 -l 40
               - - _ - -1- - _ - -2- - _ - -

A trailing space is converted to a visible character for glancing readability.
       
    $ ./ruler -l 8
    - - _ -.


