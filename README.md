# GradleIssues7593Reproduct
reproduct gradle issues 7593 example project
# How to reproduct error
Exec `./gradlew build` in terminal.
# How to fix it
annotation this line in build.gradle
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