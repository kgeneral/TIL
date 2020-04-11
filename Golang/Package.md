# Package strategy

## export function
- Use *uppercase character* for function name 
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
