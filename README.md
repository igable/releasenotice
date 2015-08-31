releasenotice
=============

This is a rough little python script for automating notices of the release of software products to slack channels.


Install
-------

    git clone https://github.com/igable/releasenotice.git
    pip install Slacker argparse
    
Configure
---------

Edit the config file with you messages and your slack API key:

    vim releasenotice.conf
    

Run
---

Post the message:

    ./releasenotice --config-file releasenotice.conf --product mixcoatl --version 1.2.0