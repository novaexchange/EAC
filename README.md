EarthCoin integration/staging tree
================================

http://www.getearthcoin.com/

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2013-2014 EarthCoin Developers

What is EarthCoin?
----------------

EarthCoin (EAC) - EarthCoin is a new generation of scrypt coin that is descendant of Litecoin. Like Litecoin it uses scrypt as a proof of work scheme.

EarthCoin uses yearly period. Start with 10000 coins per block, it varies in a sine curve with amplitude of 2000, with a period of one year (like the Earth moving around the Sun). This means that you start with 10000 coins, and it adjust at each block, reaches maximum of 12000 coins per block after about 3 months, then going down gradually, reaches 10000 coins per block again at about 6 months, then going down further, reaches the minimum point of 8000 coins per block at about 9 months, then start to going up, and return to 10000 coins per block at one year, before cutting half in payout.

EarthCoin provides superblock Awards. The following super reward zones are added:

Every 14 days there will be one day with X2 payout.
Every 31 days there will be one day with X5 payout.

Day 1 - Day 3 are special super rewards days to celebrate the launch of the coin, and provide incentive to the early adopters.

Day 1: X5 payout
Day 2: X3 payout
Day 3: X2 payout

Other Specifications:
  - 60 seconds block target
  - Difference retargets each block
  - Total coins will be 13.5 billion coins
  - 5 confirmations for transaction
  - 50 confirmations for minted blocks
  - support transaction message
  - normal block on average 10000 coins per block, varies seasonly
  - The block payout will be halved every year, minimum payout 1 coin per block

  - The default ports are 15677 (Connect) and 15678 (RPC)

For more information, as well as an immediately useable, binary version of
the EarthCoin client sofware, see http://www.getearthcoin.com/.

License
-------

EarthCoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the EarthCoin
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
regularly to indicate new official, stable release versions of EarthCoin.

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

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./earthcoin-qt_test

