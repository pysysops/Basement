Basement
------------------------------------------------------------------------

What is it?
------------------------------------------------------------------------
Basement is a webapp built in flask to allow for the easy addition of webscrapers to a database and search framework.
Currently only a pastebin scraper has been built.

Basement used both PostgreSQL and Elasticsearch as databases. Elasticsearch for efficient searching of data stored
and Postgresql as a backup in the event that Elasticsearch may want to be reindexed.

Web requests can also be forced to run through Tor.

In this form it is designed to be run on Macintosh OSX but little modification needs to be done to make it run on
Ubunutu.

Licence
------------------------------------------------------------------------
MIT License

Copyright (c) 2016 Ryan Arthur Robert Rushton

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Installation
------------------------------------------------------------------------
Please see the requirements.txt file for python packages required.
Elasticsearch, Tor and PostgreSQL are also required.

How to run?
------------------------------------------------------------------------
First install a virtual environment using python 3, I used one called virtual_env.
Then install the libraries outlined in requirements.txt.
Ensure postgresql is installed and a table exists called basement. On OSX I used the PostgreSQL app. Config for
postgres is in the config.py file.
Run the db_create.py script.
Make sure elasticsearch is installed and the path to the executable is included in app/__init__.py file. I used the
homebrew install for OSX.
Finally using the virtual environment envoke the run.py file.
