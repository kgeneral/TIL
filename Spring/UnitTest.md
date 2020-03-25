# unit test

## Spring boot 2(upper 2.2) + Junit5
- Check and change package name for major annotations
```Java
// usually org.junit -> org.junit.jupiter.api
org.junit.Test -> org.junit.jupiter.api.Test
```
- Trigger function required in gradle config
```gradle
// ...

test {
    useJUnitPlatform()
    // ...
}

// ...
```
