# htmlcolor

Html syntax highlighter for Go

## Installation

```
go get github.com/x86kernel/htmlcolor
```

## Example Code


``` go
package main

import (
        "bytes"
        "fmt"
)

import "github.com/x86kernel/htmlcolor"

func main() {
        htmlformatter := htmlcolor.NewFormatter()

        testhtml := []byte("<html>\n<head>\n<body>\n</body>\n</head>\n</html>")

        buffer := bytes.NewBuffer(make([]byte, len(testhtml)))
        htmlformatter.Format(buffer, testhtml)

        fmt.Println(buffer)
}
```
