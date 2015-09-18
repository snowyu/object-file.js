## object-file [![npm][npm-svg]][npm]

[![Build Status][travis-svg]][travis]
[![Code Climate][codeclimate-svg]][codeclimate]
[![Test Coverage][codeclimate-test-svg]][codeclimate-test]
[![downloads][npm-download-svg]][npm]
[![license][npm-license-svg]][npm]

[npm]: https://npmjs.org/package/object-file
[npm-svg]: https://img.shields.io/npm/v/object-file.svg
[npm-download-svg]: https://img.shields.io/npm/dm/object-file.svg
[npm-license-svg]: https://img.shields.io/npm/l/object-file.svg
[travis-svg]: https://img.shields.io/travis/snowyu/object-file.js/master.svg
[travis]: http://travis-ci.org/snowyu/object-file.js
[codeclimate-svg]: https://codeclimate.com/github/snowyu/object-file.js/badges/gpa.svg
[codeclimate]: https://codeclimate.com/github/snowyu/object-file.js
[codeclimate-test-svg]: https://codeclimate.com/github/snowyu/object-file.js/badges/coverage.svg
[codeclimate-test]: https://codeclimate.com/github/snowyu/object-file.js/coverage


Object-Oriented Folder/Directory Class.

* Each folder are an object.
* Each folder object could have many attributes.
  * It could be all defined in the index file(`README`) or `.value` file of a folder.
  * It could be defined in the attribute files(`.[AttributeName]`) of a folder separately.
  * The separately attributes priority is greater than the attributes in the index file.
  * The attribute could be an object(folder) too.
* The folder(directory) tree is the inheritance tree of the object.


## Mechanism

* LRU Cache
  * All file objects are cached into a global LRU Cache.
  * Some parent object could not be in memory always.

### Inheritance

* The child object inherits all attributes of the parent object by default.
* The parent object can disable some attributes to be inherited by child(not allowed to be inherited).
  * Inheritable


### Object on file system

* The folder name is an object name.
* The attribute name starts with the dot('.') char.
* The extension name means the format of the contents.


## Usage

```coffee
register  = require 'object-file'
```

## API


### attributes

The dynamic attributes of an object.
Howto merge these attributes into an object directly?

### attribute(aName[, aValue])

get or set a dynamic attribute.

* getAttribute(aName)
* setAttribute(aName, aValue)

### find(aPattern, aCount, aSkipCount)

find the specified pattern's the children of an object.


### getFolder(aPath)

get an object.

### createFolder(aPath)

## TODO


## License

MIT
