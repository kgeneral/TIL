# Struct

## With json parser
- Set first character *uppercase* for json field name
```Go

type Response struct {
	Status  string `json:"status"`
	Message string `json:"message"`
}

data := []byte(`
{
    "status": "200",
    "message": "Well done."
}
`)

var resp Response

err := json.Unmarshal(data, &resp)
if err != nil {
  log.Fatal(err)
}
fmt.Printf("%+v", resp)

```
