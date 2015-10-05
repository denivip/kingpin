# Kingpin CHANGELOG

## 0.3.1

### Changed

- `ENABLE_BITCODE` option for iOS framework is added, deployment target is set to 8.0

### Fixed

- Issue [#107: NaN at some values](https://github.com/itsbonczek/kingpin/issues/107) related to the kingpin crashing in application that uses PureLayout and exotic lifecycle management

## 0.3.0

### Added 

- OS X support is added. The only thing missing from iOS is support of animations. 
- OSX and OSX-Swift example applications are added.
- build.sh script to build frameworks for 4 targets is added: iOS, iOS-Swift, OSX, OSX-Swift.
- kingpin.xcodeproj is now `kingpin-dev.xcodeproj` that is inside `kingpin-dev` folder.
- Another Xcode project: `kingpin-examples` to hold 4 examples working against kingpin iOS and OSX frameworks is added. This is done to completely separate `kingpin-dev` project having developer targets that build kingpin from source and `kingpin-examples` project which has end-user targets that use kingpin as framework.

## 0.2.5

### Fixed

* 2 Analyzer warnings: "Function call argument is an uninitialized value (within a call to)". Both are bugs in analyzer, so radar was opened and hacks to suppress warnings were added (#69).
* Fixed Xcode warning complaining about NSParameterAssert misusing %s in its internals.

## 0.2.4

### Added

* Added Swift version of tester project to Kingpin's demo project (#80).

### Fixed

* Added import of MapKit/MKAnnotation to kp_2dtree (#82, thanks to @GabrielCartier).

## 0.2.3

### Changed

* Radius on KPAnnotation now measures from center point to farthest point. Changed Radius from a `float` to a `CLLocationDistance` to preserve accuracy (#81, thanks to @joshuadutton).

## 0.2.2

### Changed

* Updated podspec platform to `:ios, 6.0` for compatibility with Swift.

## 0.2.1

### Added

* Added a method to force refresh without any check (#78, thanks to @GabrielCartier).

## 0.2

### Added

* Add a delegate callback after map view annotations are updated (#60 and #72).

### Changed

* Much faster tree building algorithm for KPAnnotationTree is introduced.
* KPAnnotation was rewritten to use iterative preorder instead of recursion for tree traversal (#51, thanks @sammio2).
* Clustering algorithm is extracted into separate class KPGridClusteringAlgorithm.
* Unit-tests are added. The project is now built on Travis.

### Fixed

* Fixed bug on attempts to use Kingpin with map view with zero rect.

## Versions 0.1.3-0.1.4

### Fixed

* Bug with cluster grid not freed correctly (#41)

## Version 0.1.2

### Added

* support for 3D maps

## Version 0.1.1

### Added

* support for multiple tree controllers

## Versions prior to 0.1.1

Long-long history undocumented...

