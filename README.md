# ejson
enhancement of standard json library


### 
add `omitin` and `omitout` tags. for example:

```go

type T struct {
	F1 int    `json:f1,omitin`
	F2 string `json:f2,omitout`
}

```

- `omitin` specify that the field is omitted when Unmarshal
- `omitout` is like `omitin`, but is omitted when Marshal, no matter the field is 
empty or not.