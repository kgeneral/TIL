# Package strategy

## export function
- callable function for other packages
- Use first character as *uppercase* for function name to export.  
```Go
package dataparser

// private
func init() {
  //...
}

// exported
func GetData() string {
  //...
}
```
