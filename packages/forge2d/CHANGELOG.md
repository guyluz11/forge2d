## 0.11.0

> Note: This release has breaking changes.

 - **FEAT**: allowed specifying `BodyDef` properties via constructor (#51). ([aa3f5f7c](https://github.com/flame-engine/forge2d/commit/aa3f5f7cd604f1c7e3a8d90622dea812e3c63566))
 - **FEAT**: allowed specifying `FixtureDef` properties via constructor (#52). ([1c09a139](https://github.com/flame-engine/forge2d/commit/1c09a1395deb97b53638791238ab094870a201b8))
 - **BREAKING** **FEAT**: allow modifying gravity in the x-axis and y-axis (#53). ([c14b4245](https://github.com/flame-engine/forge2d/commit/c14b4245bd86f78418eb38a20ba0f0a62061af4f))
 - **BREAKING** **FEAT**: made default friciton 0 (#54). ([e943a567](https://github.com/flame-engine/forge2d/commit/e943a567483510dcebd08bc8e5d4b53366670c67))

## 0.10.0

> Note: This release has breaking changes.

 - **REFACTOR**: moved Joint render method implementation (#49). ([b9128e5a](https://github.com/flame-engine/forge2d/commit/b9128e5a589140b596cf377faeaaf1140ada3c9e))
 - **REFACTOR**: removed mock instances (#48). ([6fdf5646](https://github.com/flame-engine/forge2d/commit/6fdf5646a36b2749481269bfc56a0b88f35516c3))
 - **BREAKING** **REFACTOR**: made `createJoint` use `Joint` over `JointDef` (#50). ([0e8f3655](https://github.com/flame-engine/forge2d/commit/0e8f3655b75d1c7c516b0ac79c7b6bde54fd3fcf))
 - **BREAKING** **FEAT**: remove `JointType` (#45). ([42a39524](https://github.com/flame-engine/forge2d/commit/42a395241bb9c70932a1bbf6e84f936b52965d35))

## 0.9.0

# CHANGELOG

## 0.8.2
 - Fix `ConcurrentModificationError` when destroying a body with joints

## 0.8.1
 - Export `settings.dart`
 - Make fields in `settings.dart` mutable

## 0.8.0
 - Move `velocityIterations` and `positionIterations` to settings instead of `stepDt`
 - Make `settings.velocityThreshold` mutable

## 0.7.3
 - Fix bug with the hull creation of `PolygonShape`

## 0.7.2
 - Use field getters on getter methods where computation is O(1)

## 0.7.1
 - Fix area for polygon that is defined counter-clockwise

## 0.7.0
 - Refactored the particle system
 - Cleaned up the code and remove buffer_utils
 - Fixed y-flip to only be used on getScreenToWorld and getWorldToScreen
 - Removed the get prefix from getScreenToWorld and getWorldToScreen
 - Move debug draw methods to respective classes
 - Move web dependencies to example
 - Stable null-safety release

## 0.6.5
 - Consider y-flip for all translation in the viewport
 
## 0.6.4
 - Consider y-flip in ViewportTransform

## 0.6.3
 - Remove faulty assert in world.destroyJoint

## 0.6.2
 - One more bug fix with deleting contacts when called Body.removeFixture() when it's in contact

## 0.6.1
 - Fix bug that throws error during World.destroyBody(), Body.setType() and Body.setActive() if body has some contacts

## 0.6.0
 - Refactor joints, fixtures and contacts not to be linked lists
 - Make force/impulses default to the center of a body

## 0.5.0
 - Rebranding to forge2d
 - Make code more like the dart standard and less C++

## Old box2d.dart

### 0.4.6
* Fix bug with torque not being modified from applyTorque

### 0.4.5
* Fixing warnings and formatting

### 0.4.1 - 0.4.4
* Updates related to Flame interop + bugfixes

### 0.4.0

* Breaking: Made package strong-mode compliant 
  (with `implicit-casts` and `implicit-dynamic` off). This means many API points
  are now more strongly typed (`num` is now `double`). Fix errors by providing
  doubles where they are expected (`1` will become `1.0` and 
  `num fraction = .5` will become `double fraction = .5`), and explicitly 
  casting joints (`world.createJoint(jointDef) as RevoluteJoint`).
* Pulled in optimizations and bug fixes from the original jbox2d project.
* Made `velocityThreshold` mutable (as per jbox2d and other box2d 
  implementations).

### 0.3.0

* Updated to vector\_math 2.0.0

### 0.2.0

* Complete re-write. Many APIs have changed.
