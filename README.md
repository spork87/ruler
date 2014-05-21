ruler - a guide for terminal widths
===================================

A character ruler could be used in the status line of `tmux` or `screen` or as
part of a command line Twitter client.

An 80 column wrap is a convention, but sometimes you want an abitrary length or
the full terminal width.

An offset could be used to match width of shell prompt and script name.

With no argument `ruler` will determine the terminal environment and fit the
width, or set the length to 80 if no terminal environment exits.

Options
-------

    $ ./ruler.py -h
    usage: ruler.py [-h] [-i] [-o OFFSET] [-l LENGTH]

    Make a ruler of characters; terminal width is default

    optional arguments:
      -h, --help            show this help message and exit
      -i, --info            Show info about terminal height and width
      -o OFFSET, --offset OFFSET
                            Use spaces to offset the ruler start
      -l LENGTH, --length LENGTH
                            Length of ruler in characters

Usage
-----
    $ ruler
    ----.----1----.----2----.----3----.----4----.----5----.----6----.----7----.---_8_---.----9----.----a--

    $ ruler -i
    (75, 102)

    $ ruler -o 10
              ----.----1----.----2----.----3----.----4----.----5----.----6----.----7----.---_8_---.----9--

    $ ruler -l 81
    ----.----1----.----2----.----3----.----4----.----5----.----6----.----7----.---_8_ 

    $ ruler -o 11 -l 40
               ----.----1----.----2----.----3----.----4

