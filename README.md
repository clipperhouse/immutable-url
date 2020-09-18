A fork of [net/url](https://golang.org/pkg/net/url/) with immutable patterns for URLs.

To "mutate" a URL's Query string, you will take the query, mutate it, and then
call SetQuery, which will return a new immutable URL.

```go
import "github.com/clipperhouse/immutable-url"

u := url.Parse("https://foo.com/bar?abc=123")

q := u.Query()
q.Set("abc", "456")

u2 := u.SetQuery(q)
```

SetPath is a similar idea.