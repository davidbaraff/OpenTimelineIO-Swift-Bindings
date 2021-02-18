
# OpenTimelineIO Swift Bindings

This project provides idiomatic Swift bindings for the open source OpenTimelineIO
library.

## Prerequisites

Xcode 12.3 is the minimum Xcode requirement in order to get a version of the
Swift Package Manager that supports hybrid C++/Swift builds.

## CLI Swift Package Manager Example
====================================

If you copy/download `Examples` (`Examples` is a top-level folder of this repository)
you can play around with some simple CLI samples that show off building with SPM.

For example, put a copy of `Examples` in /home/some-user, and then:

Then:
```
    $ cd /home/some-user/Examples
    $ swift build
    (output)

    $ .build/debug/cxx_opentime_example
    (output)

    $ .build/debug/cxx_example
    (output)

    $ .build/debug/swift_example
    (output)
```
    
## OpenTimelineIO Swift Test Suite
==================================

You can also build and test the Swift OpenTimelineIO module
(which requires building the C++ core library, but does not involve Python or any other language)
from the command line easily as well:
```
    $ git clone https://github.com/OpenTimelineIO/OpenTimelineIO-Swift-Bindings.git --recurse-submodules
    ...

    $ cd Opentimelineio
    $ swift build	    # optional: swift test will do a build anyway, as needed
    ...

    $ swift test
    ...
    Test Suite 'testTransform' passed at 2020-12-13 09:54:49.488.
	    Executed 5 tests, with 0 failures (0 unexpected) in 0.001 (0.001) seconds
    Test Suite 'OpenTimelineIOPackageTests.xctest' passed at 2020-12-13 09:54:49.488.
            Executed 57 tests, with 0 failures (0 unexpected) in 1.690 (1.692) seconds
    Test Suite 'All tests' passed at 2020-12-13 09:54:49.488.
            Executed 57 tests, with 0 failures (0 unexpected) in 1.690 (1.693) seconds
```	     
	 
## Use within Xcode
====================

Use the Package Manager in Xcode and bring in
  `git@github.com:OpenTimelineIO/OpenTimelineIO-Swift-Bindings.git` with branch set to `main`.

You should see a choice of two C++ products that can be added to your workspace;
for Swift development, choose the third product named `OpenTimelineIO`.
