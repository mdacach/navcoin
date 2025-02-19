Navcoin Core integration/staging tree
=====================================

Navcoin Core is a fork of [Bitcoin Core](https://github.com/bitcoin/bitcoin). This
repository hosts the source code for the next version of Navcoin Core, which is *not
ready for production yet*. 

https://navcoin.org

For an immediately usable, binary version of the Navcoin Core software, see
https://navcoin.org/get-started.

Further information about Navcoin Core is available in the [doc folder](/doc),
the [wiki](https://github.com/navcoin/navcoin/wiki) and the [documentation website](https://doc.nav.community).

What is Navcoin?
----------------

Navcoin is an experimental digital currency that enables privacy-enhanced payments to
anyone, anywhere in the world. Navcoin uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Navcoin Core is the name of open source
software which enables the use of this currency.

License
-------

Navcoin Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built (see `doc/build-*.md` for instructions) and tested, but it is not guaranteed to be
completely stable. [Tags](https://github.com/navocin/navcoin/tags) are created
regularly from release branches to indicate new official, stable release versions of Navcoin Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md)
and useful hints for developers can be found in [doc/developer-notes.md](doc/developer-notes.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The CI (Continuous Integration) systems make sure that every pull request is built for Windows, Linux, and macOS,
and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[Navcoin Core's Transifex page](https://www.transifex.com/navcoin/navcoin/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.
