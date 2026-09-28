# Chapter 1 Project

Create the Spring Boot project here when beginning Checkpoint 1.

Suggested package: `com.ddialab.chapter01`

Initial endpoint:

```java
@RestController
public class DocumentController {
    @GetMapping("/documents/{id}")
    public Map<String, String> document(@PathVariable String id) {
        return Map.of("id", id, "content", "DDIA notes");
    }
}
```

Test:
```bash
curl -i http://localhost:8080/documents/123
```

Success means HTTP 200. Stop there for the first session.
