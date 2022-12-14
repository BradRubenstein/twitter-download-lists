# Download Twitter Follows and Lists

A simple Twitter App to export a list of your own friends, followers, blocks, and list members.

## For Programmers

This is just a few dozen lines of python that use the V1 Twitter
API.  You need to be comfortable creating an app in the Twitter
developer portal, and dealing with python scripts.

If you're not a programmer, you can export friends and followers lists using
this online tool: [CommentPicker Twitter Export](https://commentpicker.com/twitter-export.php)
(but it doesn't download list membership).

Instructions to create a new Twitter app are at
[Python Twitter: Getting Started](https://python-twitter.readthedocs.io/en/latest/getting_started.html).  You
need to have the Twitter developer portal issue four tokens, two
for the app you just created, and two to give the app permission
to read your account.  These four tokens go into the .env file.

```sh
% python3 -m venv .venv # create virtual environment
% pip install -r requirements.txt
% cp .env.example .env
% edit .env # type in tokens from the Twitter developer app: both for you as developer and you as user
% ./downloadlists
Saving output to twitter-lists-BradRubenstein-20221105T133202Z.csv...
```

Note: the program will sleep to accommodate Twitter's rate limiting. So it may take a while.
