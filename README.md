# gorm-zerolog
Zerolog logger for gorm v2

```go
package main

import (
  "gorm.io/gorm"
  "gorm.io/driver/sqlite"
  "github.com/wei840222/gorm-zerolog"
)

func main() {
  db, err := gorm.Open(sqlite.Open("test.db"), &gorm.Config{
    Logger: gorm_zerolog.New(),
  })
  if err != nil {
    panic("failed to connect database")
  }
}
```
