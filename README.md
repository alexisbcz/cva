# cva

Build class names from variants, like class-variance-authority.

## Install

```sh
go get github.com/alexisbcz/cva
```

## Use

```go
package main

import (
	"fmt"

	"github.com/alexisbcz/cva"
)

var button = cva.New("inline-flex items-center", cva.Config{
	Variants: cva.Variants{
		"size": {"default": "h-9 px-4", "sm": "h-8 px-3"},
	},
	Defaults: cva.Selection{"size": "default"},
})

func main() {
	fmt.Println(button.Classes(cva.Selection{"size": "sm"})) // inline-flex items-center h-8 px-3
}
```

## License

MIT. See [LICENSE](LICENSE) and [NOTICE](NOTICE).
