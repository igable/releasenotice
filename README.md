releasenotice
=============

This is a rough little python script for automating notices of the release of software products to slack channels.


Install
-------

    git clone https://github.com/igable/releasenotice.git
    python setup.py install
    
or get it from py PyPI

    pip install -U releasenotice
    
    
Configure
---------

Edit the [config file](https://github.com/igable/releasenotice/blob/master/releasenotice.conf)
with you messages and your slack API key:

    vim releasenotice.conf

You can set the channel for the message, the bot name, and the emoji used.

Run
---

Post the message:

    releasenotice --config-file releasenotice.conf --product exampleproduct --version 1.0.0
    
    
or load the config file from a URL. In this case you must set the environement variable `SLACK_API_KEY`, **don't post your
Slack API key** to the web in the config file accidentally.

    export SLACK_API_KEY=xoxp-0123456789-0123456789-0123456789-123a456
    releasenotice --http-config-file https://gist.githubusercontent.com/igable/x/raw/y/releasenotice.conf --product mixcoatl --version 1.2.0
    

    
    

You will get a slack message like this:

![shipitmessage](https://www.evernote.com/shard/s47/sh/1531f66b-f180-4947-9a8f-33ef2c5b446d/2ccd17b40958171f/res/6152fd6d-6c78-4585-9591-24da92a781a5/skitch.png)