# Template Maven Library

This is a dummy repository base for building a Maven library or project. You can fork this on GitHub
to make your own project base quickly.

## Features

- Configured as a parent project to allow for multiple submodules if needed.
- Enforces the Google Style Guide via Checkstyle and EditorConfig.
- Maven plugins for Surefire, Compiler, and JAR are up-to-date.
- Defaults to Java 11, but is able to change with a single property.
- Maven Wrapper is configured.
- Version information is automatically injected into any generated JARs.
- JARs are sealed to prevent other JARs from declaring the same packages at runtime.

## Things to update before you start

After you fork this project, you want to change a few things first.

1. In the root `pom.xml`:
    - Change the `java.version` property to the target Java version you want to use.
    - Change the `groupId` tag.
    - Change the `artifactId` tag.
    - Change the `version` tag if you wish to use a different versioning system.
    - Change the `name` tag.
    - Change the `description` tag.
    - Change the `license` tag.
    - Change the `scm.url` property.
    - Set the project inception year property to the current year.
    - If you do not want to use JUnit and AssertJ, remove those dependencies. If not, update them to
      the most recent version you want to use.
    - If you do not want to have a parent project with multiple submodules, then remove
      the `<packaging />` tag entirely.
2. In `.mvn/wrapper/maven-wrapper.properties`
    - Ensure the URI to the Maven distribution to use is the latest version of Maven.
3. Set the license.
    - Remove the `LICENSE.txt` if you are using GPL, and replace with corresponding
      `COPYING` and `COPYING.lesser`.
    - ...or for anything else, replace `LICENSE.txt` with your desired license. You do not have to
      credit me or anything, I don't care about that in this project.
4. Set the license header in `.mvn/checkstyle/license-header-java-groovy-kotlin-scala.txt`.
5. If you do not want the Google code style to be enforced:
    - Change the `.mvn/checkstyle/checkstyle.xml` and `.mvn/checkstyle/suppressions.xml`.
    - Update the `.editorconfig` accordingly.
    - Reformat all files in your IDE.
6. Update the `.github/workflows/commit.yml` to use the appropriate Java version, or replace it
   with whatever you want to do.
7. Replace this `README.md`.
