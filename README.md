![example workflow](https://github.com/AS131986/APICI/actions/workflows/gradle.yml/badge.svg)

image: Ubuntu

stack: jdk 11

branches:
  only:
    - master

build: off

install:
  - java -jar ./artifacts/app-mbank.jar &

build_script:
  - ./gradlew test --info
