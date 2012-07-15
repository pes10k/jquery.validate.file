# jquery.validate.file.js

File validation methods for the jQuery Validation plugin

## About

This library adds several validation methods to the [jQuery Validation plugin](http://bassistance.de/jquery-plugins/jquery-plugin-validation/).  Specifically, the following validation methods are provided:


### "fileType"

Validates that an selected file is of a given file type, as determiend by it's
reported mime string.

It accepts one optional configuration parameter

*   *types* : **array** (default ["text"])

    An array of file types.  This types are loosely checked, so including
    "text" in this array of types will cause "text/plain" and "text/css"
    to both be excepted.  If the selected file matches any of the strings
    in this array, validation passes.


### "minFileSize"

Validates that a file selected for upload is at least a given file size.

It accepts two optional configuration parameters

*   *unit* : **string** (default "KB")

    The unit of measure of the file size limit is in.  Valid inputs
    are "B", "KB", "MB" and "GB"

*   *size* : **number** (default 100)

    The minimum size of the file, in the above units, that the file
    must be to be accepted as "valid"

### "maxFileSize"

Validates that a file selected for upload is no larger than a given file size.

It accepts two optional configuration parameters

*   *unit* : **string** (default "KB")

    The unit of measure of the file size limit is in.  Valid inputs
    are "B", "KB", "MB" and "GB"

*   *size* : **number** (default 100)

    The maximum size of the file, in the above units, that the file
    can be to be accepted as "valid"

## Author

Peter E. Snyder - snyderp@gmail.com