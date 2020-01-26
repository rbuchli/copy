# copy

[![Build Status](https://travis-ci.org/otiai10/copy.svg?branch=master)](https://travis-ci.org/otiai10/copy)
[![codecov](https://codecov.io/gh/otiai10/copy/branch/master/graph/badge.svg)](https://codecov.io/gh/otiai10/copy)
[![GoDoc](https://godoc.org/github.com/otiai10/copy?status.svg)](https://godoc.org/github.com/otiai10/copy)
[![Go Report Card](https://goreportcard.com/badge/github.com/otiai10/copy)](https://goreportcard.com/report/github.com/otiai10/copy)

`copy` copies directories recursively.

Example:

```go
err := Copy("your/directory", "your/directory.copy")
```

This is just a copy of the well documented original repository, but with one extension:
The copy is done with a prefixed "\\\\?\\". This is done to overcome the windows file path restriction of 260 characters. With this, the limit is 32000 characters.
This is needed for example to copy data directories from other solutions (like Alfresco) in Windows. Without this change, the copy of longer pathnames than 260 chars will fail. 
