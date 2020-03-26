# Jackson

## Deserialize with constructors only(without setter)
```Java
@Getter
public class PersonDto {
  String firstName;
  String lastName;
  
  // empty constructor is mandatory
  public PersonDto() {}
  
  public PersonDto(String firstName, String lastName) {
    // ..
  }
}
```
