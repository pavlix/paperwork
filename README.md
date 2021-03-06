# Invoice

This is my quick and dirty invoice system I am going to use for my invoices
in year 2012.

The program is higly experimental and users are expected to know at least a
bit of Python coding. Feedback is appreciated.

Pavel Šimerda

## License

This version of the source code is released into public domain, future releases
may adopt a BSD-like license.

## Requirements

 * Python 3.2
 * python3-tempita 0.5.1
 * pdflatex

## Installation

You don't need to install, just make a symlink to the invoice script
in `~/bin` or `/usr/bin/local`.

You will need to make the following symlinks or directories in ~/.invoice/

 * data (the database)
 * data/$YEAR (current year)
 * tmp
 * output
 * output/$YEAR

Use the code or error messages in case this list is incomplete. Use -D for
debugging.

## User configuration

For now an empthy `~/.invoice/config` should do.

## Basic usage

Export `EDITOR` and `PDF_VIEWER` environment variables to choose your favourite
text editor and PDF viewer. Defaults are 'vim' and 'xdg-open'.

Manage companies:

invoice new-company <id>
invoice edit-company <id>
invoice show-company <id>
invoice delete-company <id>

Manage invoices:

invoice new <company-id>
invoice edit [<number>]
invoice show [<number>]
invoice delete [<number>]

Generate and display invoice PDF:

invoice pdf --generate [<number>]
