# springvalidation

Bean validation in Spring Boot: `hibernate-validator` constraints on a form object, and the part
that actually matters — getting the messages back onto the page next to the fields.

## What is in here

- `entities/LoginData.java` — the constrained bean (`@NotBlank`, `@Size` and friends)
- `controller/MyController.java` — `@Valid` plus a `BindingResult`, returning the user to the form
  when it fails rather than throwing
- `templates/form.html` — Thymeleaf rendering the per-field errors
- `templates/success.html` — the path taken when validation passes

Spring Boot with Thymeleaf. No database.

### Running it

```bash
./mvnw spring-boot:run
```
Then open http://localhost:8080.

---

One of a set of small repositories I wrote while learning the Java/Spring ecosystem. Each one
exists to get a single idea working end to end, so it is deliberately minimal — no tests worth the
name, no production hardening. Kept public because the commit history is a more honest record of
what I learned than a summary would be.
