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
class SqlTemplate(@Value("\${table.schema}") private var tableSchema: String) {
    fun getMemberAgeForId(): String = "select age from $tableSchema.member where id = ?"
}
```
