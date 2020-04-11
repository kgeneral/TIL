# Package strategy

## export function
- callable function for other packages
```Go
package data_parser

// private
func init() {
  //...
}

// exported
func GetData() string {
  //...
}
```
