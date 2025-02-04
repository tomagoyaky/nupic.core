# Changelog

## 0.4.1

* Cast arg to UInt32 to avoid call resolution ambiguity on the value.write() method on Win32 platform.
* Finish adding support for the Bool type
* Expose encoder's 'n' so other regions' inputWidth is calculable from the outside
* Remove reference to deleted Linear.cpp.
* Run nupic.core encoders via boilerplate Sensor wrapper
* Removes Linear.hpp, Linear.cpp, and reference in algorithms.i since it doesn't appear to be used anywhere.
* Support Debug builds in Clang, put them in README
* Add a NTA_BasicType_Bool so that we can parse bools in YAML
* FloatEncoder base, no more common Encoder, new signature
* Prepends BINDINGS_VERSION plus dot separater to wheel filename
* Fix integer division bug, add tests that would catch this bug
* Don't divide by a constant. Multiply. Dodges divide-by-0.
* Explicitly mark all derived virtual methods as virtual.
* Fix gcc build issue
* C++ Encoder base + ScalarEncoder + ported unit tests

## 0.4.0

* Reduce EPSILON threshold for TM to minitage compatibility issues.
* Updates AV yaml to push a commit-sha'd wheel to AWS
* Reduce permanence threshold by epsilon before comparing to avoid rounding edge cases
* Make threshold for destroying synapses larger to catch roundoff errors
* Make comparison identical to python
* Add accessors for TM columnForCell and cellsForColumn
* Temporal Memory: recordIteration should be false in second call to computeActivity
* Fix: Incompatibility in Connections.computeActivity with python
* Change TM init parameters to accept segment and synapse limit.

## 0.3.1

* Secondary sort on segment idx
* Sort segments before iterating for python compatibility
* Sort unpredictedActiveColumns before iterating for python compatibility

## 0.3.0

* Updated SWIG bindings for accessors
* Added TemporalMemory accessors
* Update bindings for C++ Connections to expose 'read' class method
* Destroy lowest permanence synapse when synapse limit is reached
* Fix for bug in Segment::freeNSynapses
* Added initialization code from Tester::init into PathTest::PathTest that is required for PathTest::copyInTemp to run successfully.
* Remove references to Tester from UnitTestMain.cpp
* Deleted Tester class and TesterTest files
* Update SWIG binding of Network to add read class method
* Refactor PyRegion subclasses to take specific proto object in read
* Update SWIG binding of TemporalPooler to add read class method
* Enable basic building with ninja (cmake -GNinja)
* Added include of Log.hpp in NodeSet.hpp
* Update SWIG bindings of SpatialPooler and CLAClassifier to add read class methods to C++ classes

## 0.2.7

* Full filename for twine.
* Absolute path for twine's binary file upload.

## 0.2.6

* Fixed incorrect binary path for twine.

## 0.2.5

* Fixing twine upload of windows binary.

## 0.2.4

* Working out issues with the release process.

## 0.2.3

* Windows Support!
* Add bindings for CLAClassifier serialization
* Adding Windows twine pip install and PyPi upload
* Storing release version in VERSION in proj root.
* Makes build-from-source the default behavior for capnp and swig, requiring the flags FIND_CAPNP or FIND_SWIG to be specified in order to use a preinstalled version.
* Add Dockerfile for building nupic.core from source
* Update of Windows bindings setup
* Add "python setup.py test" option (fixes #697)
* Adding a CMake ExternalProject to download capnp win32 compiler tools
* Simplify setup.py, remove unused command line args, add setup.py clean command. Update Travis to build Python extensions as part of cmake so Python install doesn't rebuild them.
* Allow finding pre-built capnp.
* Revert back to numpy==1.9.2

## 0.2.2

* First changelog entry.
