# Customize snippet

## Template
- Put your own templates in your project : test.resources.org.springframework.restodcs.templates
i.e.) https://github.com/spring-projects/spring-restdocs/blob/master/spring-restdocs-core/src/main/resources/org/springframework/restdocs/templates/asciidoctor/default-curl-request.snippet

## Custom parsing class
- Put your own class in your test.java package : org.springframework.restdocs.*
i.e.) https://github.com/spring-projects/spring-restdocs/blob/master/spring-restdocs-core/src/main/java/org/springframework/restdocs/cli/CurlRequestSnippet.java#L148
