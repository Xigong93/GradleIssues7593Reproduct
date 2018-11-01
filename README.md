# [GradleIssues7593Reproduct](https://github.com/gradle/gradle/issues/7593)
reproduct gradle issues 7593 example project.
# How to reproduct error
Exec `./gradlew build` in terminal.
# How to fix it
annotate this line in build.gradle
```groovy
buildscript {
    ext.kotlin_version = '1.2.71'
    repositories {
        //maven { url "https://maven.aliyun.com/repository/gradle-plugin" }// Annotate this line ,build will successed.
        google()
        jcenter()
    }
    ...
}

```
And then exec `./gradlew build` in terminal will success.