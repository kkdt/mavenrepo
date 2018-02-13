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

## Publish to Local Repository

```
// build.gradle (for something to publish to local repo)

apply plugin: 'maven-publish'

ext {
    localrepo = project.hasProperty('localrepo') ? localrepo : buildDir.path + "/artifacts"
}

publishing {
    publications {
        myPublication(MavenPublication) {
            // publish jar archive
            from components.java
            // include publish README.md
            artifact ('README.md') {
                classifier = 'README'
                extension  = 'md'
            }
        }
    }
    // publish artifacts to local directory
    repositories {
       maven {
          url file(localrepo)
       }
    }
}
```
