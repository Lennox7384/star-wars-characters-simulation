# Star Wars Characters Simulation

A small Java OOP exercise built around two domain classes (`Fighter`, `Force`) with a deep JUnit 4 test suite. The driver class `StarWarsMainApp` runs a deterministic fight scenario between canon Star Wars characters and demonstrates Light vs. Dark force interactions, taunts, and `Cloneable` behavior.

## Highlights

- 16 JUnit test methods covering both classes (7 for `Fighter`, 9 for `Force`).
- `Fighter implements Cloneable` with a custom `clone()` exercised under test.
- Domain rules tested directly against console output via `ByteArrayOutputStream` redirection (no mocking framework needed).
- Pure standard-library Java, no external runtime dependencies. JUnit 4 is the only test dependency.

## Layout

```
star-wars-characters-simulation/
  src/
    main/java/starwars/
      Fighter.java          # core fighter model with Cloneable support
      Force.java            # force strength + alignment model
      StarWarsMainApp.java  # demo driver with named canon characters
    test/java/starwars/
      FighterTest.java      # 7 tests (taunts, fight outcomes, clone semantics)
      ForceTest.java        # 9 tests (force level bounds, alignment rules)
  pom.xml
  LICENSE
```

## Run the demo

```bash
mvn compile exec:java
```

## Run the tests

```bash
mvn test
```

Expected: `Tests run: 16, Failures: 0, Errors: 0`.

## License

MIT. See `LICENSE`.
