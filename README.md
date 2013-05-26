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


## Example

Below is a simple, example for that will only allow the user to upload a
text, gzip or zip file that is between 10-100Kb.

```
    <form method="post" enctype="multipart/form-data" id="upload_form">
        <input type="file" name="example_file" name="example_file">
        <button type="submit">Upload</button>
    </form>


    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
    <script src="https://ajax.aspnetcdn.com/ajax/jquery.validate/1.9/jquery.validate.min.js"></script>
    <script>
    $(function () {
        $("#upload_form")
            .validate({
                rules: {
                    example_file: {
                        fileType: {
                            types: ["text", "gzip", "zip"]
                        },
                    maxFileSize: {
                        "unit": "KB",
                        "size": 100
                    },
                    minFileSize: {
                        "unit": "KB",
                        "size": "10"
                    }
                }
            });
    });
    </script>
```

## Author

Peter E. Snyder - snyderp@gmail.com
