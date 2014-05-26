MarketChange (CHG) integration/staging tree
=====================================

![Build status](https://api.travis-ci.org/MarketChange/MarketChange.svg) 

http://marketchange.github.io

Copyright (c) 2009-2013 Bitcoin Developers

Copyright (c) 2011-2013 Litecoin Developers

Copyright (c) 2014 The MarketChange Developers

Block Explorer
--------------

http://chgexplorer.tk

Pool
----

http://chgpool.tk:15437/static

Ports
-----

- RPC Port 14437
- P2P Port 14438 (Testnet: 13438)

What is MarketChange?
---------------------

MarketChange is a clone of Litecoin that is meant to make it easy for merchants to accept cryptocurrency.
 - 55 second block targets
 - subsidy lessens in 574k blocks (~1 year)
 - ~200 million total coins
 - 50 coins per block
 - 2 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the MarketChange client sofware, see http://marketchange.github.io

FAQ
---

-Why is the genesis block from so long ago?
Because I had originally started making the coin at that time, but other things got in the way so the release was held back.

-I want to donate!
Great! You can send MarketChange to this address: MREjSSg3CHZ4oDqSKCYM5RQypEZbuqRBZV

License
-------

Litecoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Litecoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=bitcoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Litecoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test marketchange-qt.pro
    make -f Makefile.test
    ./litecoin-qt_test
