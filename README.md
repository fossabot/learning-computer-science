# Learning Computer Science

![logo](https://github.com/manastalukdar/learning-computer-science/blob/master/resources/images/logo/Logo%20LCS%20color/logo%20LCS%20color%20low%20res.png?raw=true)

Learning data structures, algorithms, machine learning and various computer science constructs by programming practice from resources around the web.

## Requirements

### Development Environment

Highly recommended to open/use this repository using [Visual Studio Code](https://code.visualstudio.com/).

| Language |  Version | Package
| ---------|----------|---------
| Java | 12.0.1 | OpenJDK (Red Hat for Windows)
| Python | 3.7.2 | N/A

### Updating VSCode Extensions List

1. Get json data for list of extensions using the uploaded Sync file in GitHub.
2. Filter by `metadata.publisherId` using the website <https://jsoneditoronline.org/>.
3. Update list in file `.vscode/extensions.json`.

## Usage

### Viewing

#### Options

1. Open repository using [Visual Studio Code](https://code.visualstudio.com/). Recommended extensions have been provided by the repository (.vscode folder).
1. Use [Sourcegraph](https://sourcegraph.com/github.com/manastalukdar/learning-computer-science/).
1. A website for filtering and querying is [work-in-progress](https://github.com/manastalukdar/learning-computer-science/projects/1).

### Running Tests

1. VSCode tasks are available via the repository (.vscode folder) for running all language specific tests. Please familiarize yourself with using tasks in VSCode.

### Contributing

1. Please follow the template for adding problems. This is inherently tied into the mechanism for searching through problems using the [planned website](https://github.com/manastalukdar/learning-computer-science/projects/1).
1. Templates for metadata.json (problem metadata), readme.md (problem definition) and language specific solution and solution test files are available via VSCode snippets. They are all committed and available via the repository (.vscode folder). Please familiarize yourself with using snippets in VSCode.
1. You are encouraged to fork this repository and submit pull requests.

### Other

1. For those who may not wish to use VSCode and instead prefer a simple text editor
    1. I plan to create a [makefile](https://github.com/manastalukdar/learning-computer-science/issues/50).
    1. Instructions will be provided at a later time for command line usage to add new problems, run tests, etc. [Ref](https://github.com/manastalukdar/learning-computer-science/issues/51)
1. I do not recommend using any sort of bloated IDE. They tend to add a lot of files simply for their specific plumbing.

### Upgrading to newer versions of development environments

#### Java

1. Install latest version of Java: OpenJDK (Red Hat for Windows).
1. On Windows, update the Path environment variable to point to new Java install location. Look out for JAVA_HOME env var, and javapath in the Path env var.
1. Update build.gradle script (`sourceCompatibility` and `targetCompatibility`).
1. Download and update the (latest) version of gradle compatible with the new version of Java.
1. In Windows, update the Path environment variable to point to new gradle install location.
1. In the repository root, from admin command prompt, run `gradle wrapper --gradle-version <new gradle version>`.
1. Make sure `distributionUrl` in `gradle/wrapper/gradle-wrapper.properties` points to new gradle version.
1. Delete .project and .classpath files.
1. Delete all contents of bin directory.
1. Close VSCode.
1. Clear [workspace cache](https://github.com/Microsoft/vscode-java-debug/blob/master/Troubleshooting.md#try).
1. Restart VSCode.
1. Make sure new .project and .classpath files have been generated. Verify that .classpath now points to the new version of Java. This may take a good few minutes.
1. Run gradlew test and code coverage tasks.
1. Update CI scripts (appveyor, circle-ci, travis) to point to new Java version.
   1. For circle-ci, docker image tags can be viewed [here](https://circleci.com/docs/2.0/docker-image-tags.json).

#### Gradle

From the project root, run `.\gradlew.bat wrapper --gradle-version x.x.x`. For Linux, run gradlew from the root, instead of the .bat file. Use the desired version in the command. Verify that the `distributionUrl` field in the file `gradle-wrapper.properties` has been updated to reflect the correct version. \[[Reference](https://docs.gradle.org/current/userguide/gradle_wrapper.html#sec:upgrading_wrapper)\]

#### Python

1. Install latest version of Python.
2. Run tasks for python tests, coverage reports and problems list.
3. Update CI scripts (appveyor, circle-ci, travis) to point to new Python version.

## Continuous Integration

| Platform | Provider | Operations | Status |
|----------|----------|------------|--------|
| Windows, Linux | AppVeyor | Build, Test | [![Build status](https://ci.appveyor.com/api/projects/status/y9qup8owf4e53m8h?svg=true)](https://ci.appveyor.com/project/manastalukdar/learning-computer-science) |
| Linux | Travis CI | Build, Test, Deploy to gh-pages | [![Build Status](https://travis-ci.org/manastalukdar/learning-computer-science.svg?branch=master)](https://travis-ci.org/manastalukdar/learning-computer-science) |
| Linux | Circle CI | Build, Test | [![CircleCI](https://circleci.com/gh/manastalukdar/learning-computer-science/tree/master.svg?style=svg)](https://circleci.com/gh/manastalukdar/learning-computer-science/tree/master) |
| N/A | CodeClimate | Check for code maintainability | [![Maintainability](https://api.codeclimate.com/v1/badges/2ece575493d263e8b83c/maintainability)](https://codeclimate.com/github/manastalukdar/learning-computer-science/maintainability) |
| N/A | CodeClimate | Check for test coverage using Circle CI | [![Test Coverage](https://api.codeclimate.com/v1/badges/2ece575493d263e8b83c/test_coverage)](https://codeclimate.com/github/manastalukdar/learning-computer-science/test_coverage) |
| N/A | Codacy | Code analysis/quality check | [![Codacy Badge](https://api.codacy.com/project/badge/Grade/93f9326796aa44a3a9eac1fe9c13cc24)](https://www.codacy.com/app/manastalukdar/learning-computer-science?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=manastalukdar/learning-computer-science&amp;utm_campaign=Badge_Grade) |
| N/A | CodeBeat | Static code analysis | [![codebeat badge](https://codebeat.co/badges/882b6622-7bc2-4923-97b2-a053057d3a45)](https://codebeat.co/projects/github-com-manastalukdar-learning-computer-science-master) |
| N/A | Codecov | Code coverage using Circle CI | [![codecov](https://codecov.io/gh/manastalukdar/learning-computer-science/branch/master/graph/badge.svg)](https://codecov.io/gh/manastalukdar/learning-computer-science) |
| N/A | Coveralls | Code coverage using Circle CI | [![Coverage Status](https://coveralls.io/repos/github/manastalukdar/learning-computer-science/badge.svg?branch=master)](https://coveralls.io/github/manastalukdar/learning-computer-science?branch=master) [Known issue](https://github.com/manastalukdar/learning-computer-science/issues/35)|
| N/A | FOSSA | Open Source Software Management | [![FOSSA Status](https://app.fossa.com/api/projects/custom%2B10734%2Fgit%40github.com%3Amanastalukdar%2Flearning-computer-science.git.svg?type=shield)](https://app.fossa.com/projects/custom%2B10734%2Fgit%40github.com%3Amanastalukdar%2Flearning-computer-science.git?ref=badge_shield) |
| N/A | CII Best Practices | Open source software best practices check | [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/1761/badge)](https://bestpractices.coreinfrastructure.org/projects/1761) |
| N/A | david-dm | Check node.js dependency status | [![Dependency Status](https://david-dm.org/manastalukdar/learning-computer-science.svg)](https://david-dm.org/manastalukdar/learning-computer-science?path=website-react-next) |
| N/A | david-dm | Check node.js dev dependency status | [![devDependencies Status](https://david-dm.org/manastalukdar/learning-computer-science/dev-status.svg?path=website-react-next)](https://david-dm.org/manastalukdar/learning-computer-science?path=website-react-next&type=dev) |

<!-- waffle
ZenHub -->

## Project Management

[GitHub Projects](https://github.com/manastalukdar/learning-computer-science/projects)

## Links

[Sourcegraph](https://sourcegraph.com/github.com/manastalukdar/learning-computer-science/)

## Note

1. Problems in the repository are not necessarily solved by me. The goal is to learn. Sometimes in the interest of time, that involves understanding an existing solution rather than spending an inordinate amount of time trying to solve it by myself. Where applicable I have provided references to the original solution.
2. Problems in this repository are not unique. Given that the same (or similar) problem may exist in multiple origins, more than a few problems are repeated. It is my goal to provide some sort of querying mechanism via a [website](https://github.com/manastalukdar/learning-computer-science/projects/1) for users to view only a unique instance of a problem, either from a "first or default" origin or a specified origin.
