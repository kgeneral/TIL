# Optional

## Inproper usage for optional
- Just for single-condition before single-assignment : Optional is a **_costly_** operation.
```Java
// AVOID
String status = Optional.ofNullable(status).orElse("PENDING");
// PREFER
String status = status == null ? "PENDING" : status;
```

## Reference
- https://dzone.com/articles/using-optional-correctly-is-not-optional
- https://www.slideshare.net/gyumee/java-null-survival-guide
