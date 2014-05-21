ruler - a guide for terminal widths
===================================

An 80 column wrap is a convention, but sometimes you want an abitrary length or
the full terminal width.

Usage
-----

    ruler [-i indent] [-l length]

    $ ruler
    ----.----1----.----2----.----3----.----4----.----5----.----6----.----7----.---_8_---.----9----.----a----

    $ ruler -l 81
    ----.----1----.----2----.----3----.----4----.----5----.----6----.----7----.---_8_ 

    $ ruler -i 11 -l 40
               ----.----1----.----2----.----3----.----4

With no argument `ruler` will determine the terminal environment and fit the
width, or set the length to 80 if no terminal environment exits.
