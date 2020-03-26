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
## Mock test with 'mockwebserver' for Spring WebClient
- Basic @Mockbean is not work properly.
- Need to update 'okhttp' version in gradle(upper 3.10)
```gradle
    testImplementation "com.squareup.okhttp3:mockwebserver"
    testImplementation "com.squareup.okhttp3:okhttp:3.14.6"
```
- Test example : https://github.com/spring-projects/spring-framework/blob/master/spring-webflux/src/test/java/org/springframework/web/reactive/function/client/WebClientIntegrationTests.java
```Java

	@ParameterizedWebClientTest
	void shouldReceiveJsonAsString(ClientHttpConnector connector) {
		startServer(connector);

        // use mock json string as response.
        // specific uri is not possible. one server - one mock request
        // need to overwrite for each test case
		String content = "{\"bar\":\"barbar\",\"foo\":\"foofoo\"}";
		prepareResponse(response -> response
				.setHeader("Content-Type", "application/json").setBody(content));
        // ...
    
    
```
