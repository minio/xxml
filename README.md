# xxml

> NOTE: This package is a fork of 'encoding/xml' from https://github.com/golang/go.

Package xml implements a simple XML 1.0 parser that understands XML name spaces, 
along with extended support for control characters such as following

```
var controlCharactersMap = map[rune][]byte{
        '\x00': []byte("&#x0;"),
        '\x01': []byte("&#x1;"),
        '\x02': []byte("&#x2;"),
        '\x03': []byte("&#x3;"),
        '\x04': []byte("&#x4;"),
        '\x05': []byte("&#x5;"),
        '\x06': []byte("&#x6;"),
        '\x07': []byte("&#x7;"),
}
```

XML 1.0 spec does not allow these control characters. However this package intends 
to support these characters to satisfy MinIO's needs for AWS S3 compatiblity.
