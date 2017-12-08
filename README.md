# Cake build container

This is a Docker container with both .NET Core 1 and 2 installed to run [Cake](https://cakebuild.net/) with a .NET Core 2 project.

Uses a Ubuntu 16.04 base image.

## Sample CircleCI 2.0 Config

```yml
version: 2
jobs:
  build:
    docker:
      - image: adamhathcock/cake-build:latest
    steps:
      - checkout
      - run:
          name: Build
          command: ./build.sh
```