Tweet2IRC
==

An IRC bot which listens for Twitter keywords and shows related tweets in an IRC channel.

Features :
* IRC client with optional TLS and server password
* channel auto-join
* tweets de-dupe
* tweets rate limiting

Debian/Ubuntu dependencies :

    sudo apt-get install libanyevent-http-perl libanyevent-irc-perl

Usage :

    cp tweet2irc.cfg my.cfg
    vi my.cfg
    ./tweet2irc my.cfg

Then from your favorite IRC client :

    <user> tweety: help
    <tweety> add <rule spec>
    <tweety> del <rule id>
    <tweety> get
    <tweety> (see https://developer.twitter.com/en/docs/twitter-api/tweets/filtered-stream/quick-start)

**TODO** :
* better streaming error API handling, right now it always retry no matter what (eg: auth failed -> better take a large pause or give up)

(c) 2022 Bearstech - released under AGPL v3
