
### 경로설정
```
C:\Users\user\IdeaProjects>mkdir cms_clean

C:\Users\user\IdeaProjects>cd cms_clean
```

### 프로젝트 선택
```
gradle init --type java-library


Select type of project to generate:
  1: basic
  2: application
  3: library
  4: Gradle plugin
Enter selection (default: basic) [1..4] 1

Select build script DSL:
  1: Groovy
  2: Kotlin
Enter selection (default: Groovy) [1..2] 1

Generate build using new APIs and behavior (some features may change in the next minor release)? (default: no) [yes, no]
Project name (default: cms_clean):

> Task :init
Get more help with your project: Learn more about Gradle by exploring our samples at https://docs.gradle.org/7.6/samples

BUILD SUCCESSFUL in 13s
2 actionable tasks: 2 executed
```

C:\Users\user\IdeaProjects\cms_clean>                          

### 기본 프로젝트 경로 생성

```
└─src
    ├─main
    │  ├─java
    │  ├─resources
    │  └─webapp
    │      └─WEB-INF
    │          └─lib
    └─test
        ├─java
        └─resources
```



### build.gradle 추가
```
apply plugin: 'java'
apply plugin: 'war'
repositories {
  jcenter()
  }
dependencies {
  testImplementation 'junit:junit:4.12'
  implementation group: 'javax.servlet', name: 'javax.servlet-api', version: '3.1.0'
}

```


### 빌드 (아래 참고사항으로 진행 할 시 불필요)
```
$ gradle war 
```

### 참고사항 smart tomcat
1. intellij community 실행
2. smart tomcat plugin 설치 (setting)
3. intellij 재시작
4. setting > tomcat server add
5. intellij new project 생성
    - intellij new project > exsist source
  


