# GradleIssues7593Reproduct
reproduct gradle issues 7593 example project
issues link https://github.com/gradle/gradle/issues/7593
# How to reproduct error
Exec `./gradlew build` in terminal.
# How to fix it
annotate this line in build.gradle
```groovy
buildscript {
    ext.kotlin_version = '1.2.71'
    repositories {
        //maven { url "https://maven.aliyun.com/repository/gradle-plugin" }// when you annotation this line "./gradlew build" will success
        google()
        jcenter()
    }
    ...
}

```
And then exec `./gradlew build` in terminal will success.