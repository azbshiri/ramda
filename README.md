# ramda-go
An implemenation of ramda library for Go programmers.


# Installation
```
$ go get github.com/azbshiri/ramda
```

# Usage
```go
import "github.com/azbshiri/ramda"

func main() {
		waterTemp := ramda.NewCond(ramda.Cond{
			Equals(0), Always("water freezes at 0°C"),
			Equals(100), Always("water boils at 100°C"),
			T(), Always("nothing special happens at %d°C"),
		})
    
    fmt.Println(waterTemp(0)) # water freezes at 0°C
    fmt.Println(waterTemp(100)) # water boils at 100°C
    fmt.Println(waterTemp(50)) # nothing special happens at 50°C
    fmt.Println(waterTemp(70)) # nothing special happens at 70°C
}
```

# TODO
[ ] Add exmaples in comments