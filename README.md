# Download Twitter Follows and Lists

A simple Twitter App to download a list of friends, followers, blocks, and list members.

## For nerds only

Instructions to create a new twitter app are at
[python-twitter: Getting Started](https://python-twitter.readthedocs.io/en/latest/getting_started.html).
You need to have the Twitter developer portal issue four tokens, two for the app you
just created, and two to give the app permission to read your
account.  These four tokens go into the .env file.

```sh
% python3 -m venv .venv # create virtual environment
% pip install -r requirements.txt
% cp .env.example .env
% edit .env # type in tokens from the Twitter developer app: both for you as developer and you as user
% ./downloadlists
```

Note: the program will sleep to accommodate twitters rate limiting. So it may take a while.
