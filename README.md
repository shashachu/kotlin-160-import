# kotlin-160-import
Bug demonstrating a regression with Kotlin 1.6.0 with imports on multiple lines

# Repro
- run `./gradlew build` 
- Note you get a compile error:
```
> Task :compileKotlin FAILED
e: /Users/shasha/code/shashachu/kotlin-160-import/src/main/kotlin/me/shasha/Main.kt: (7, 16): Unresolved reference: MY_CONSTANT
```
- Change Kotlin version from `1.6.0` to `1.5.20` in `build.gradle`
- Re-build and note that the project compiles successfully
