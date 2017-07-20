# mavenrepo

Personal Maven repository for publishing `kkdt` artifacts.

## Gradle Usage

```
buildscript {
   repositories { 
      maven {
         url 'https://github.com/kkdt/mavenrepo/raw/master'
      }
   }
   dependencies {
      classpath "kkdt.gradle.api:gradleapi:0.1"
   }
}
```

