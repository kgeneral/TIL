# Spring by Kotlin

## lateinit + @Value
```yaml
# application-dev.yaml
table:
  schema: dev
  
# application-prod.yaml
table:
  schema: prod

```
```Kotlin
@Component
class SqlTemplate {

    @Value("\${table.schema}")
    private lateinit var tableSchema: String
    
    // cannot use 'val' or 'var' : 'tableSchema' loads lazy
    fun getMemberAgeForId(): String = "select age from $tableSchema.member where id = ?"

}
```
