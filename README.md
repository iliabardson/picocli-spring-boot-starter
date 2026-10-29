# picocli-spring-boot-starter

A self-contained subset of [picocli](https://github.com/remkop/picocli),
forked from upstream commit `10509c0af89aa3254ca14ba90d9b3b7168e57994`. The Git history of retained files is
preserved; filtering rewrites commit IDs.

## Build

Install JDK 17 and run:

```bash
./gradlew clean build --no-daemon
```

On Windows, run `gradlew.bat clean build --no-daemon`.
The checked-in Gradle wrapper downloads Gradle and dependencies on first use.
The build compiles production and test sources, runs tests, and builds JARs.
No sibling repository checkout or locally published picocli artifact is required.
Java 17 is the version verified locally and used by CI.

## Included source

The root `src/` contains picocli core and its tests. The Gradle root project
is named `picocli` to preserve the core's artifact name and existing module
dependencies. This repository also includes:

- `picocli-spring-boot-starter/`

Core source is intentionally duplicated across the subset repositories.
Changes to the embedded core are built together with this repository's modules.
Build artifacts are in `build/libs/` and each module's `build/libs/`.

## Documentation and origin

API Javadoc is built from the included source. Upstream documentation is retained
in `docs/`; the full upstream manual and release automation cover modules
outside this subset and are not part of its normal build.
See [UPSTREAM-README.md](UPSTREAM-README.md) for the original project overview
and [subset.json](subset.json) for the extraction manifest.

## License

Apache License 2.0; see [LICENSE](LICENSE). Upstream copyright notices and
[NOTICE-DOCS](NOTICE-DOCS) are retained.
