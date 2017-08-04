rebelsouls-versions
-

Dependency Management description.

## Usage

### Get versions in a project

```groovy
dependencyManagement {
    imports {
        mavenBom 'io.rebelsouls.lib:rebelsouls-versions:1.0'
    }
}

dependencies {
    compile 'org.springframework:spring-core'
    compile 'io.rebelsouls.lib:rebelsouls-mail'
}
```

### Updating versions

Edit `build.gradle` in this project:

```groovy
dependencyManagement {
    imports {
        mavenBom 'io.spring.platform:platform-bom:Brussels-SR1'
    }
    dependencies {
        dependency 'io.rebelsouls.lib:rebelsouls-mail:1.1'
        dependency 'io.rebelsouls.lib:rebelsouls-util:1.10'
        dependency 'io.rebelsouls.lib:rebelsouls-storage:1.1'
        dependency 'io.rebelsouls.lib:rebelsouls-users:1.2'
    }
}
```

Then release:

```bash
$ ./gradlew release
```
