# Git-describe Maven plugin

This plugin invokes `git describe` and captures the output in a build variable.

## Configuration

The plugin might be configured in your pom like so:

```xml
      <plugin>
        <groupId>com.lukegb.mojo</groupId>
        <artifactId>gitdescribe-maven-plugin</artifactId>
        <version><!-- Version --></version>
        <executions>
          <execution>
            <goals>
              <goal>gitdescribe</goal>
            </goals>
            <id>git-describe</id>
            <phase>initialize</phase>
            <configuration>
              <!-- configuration properties go here. -->
            </configuration>
          </execution>
        </executions>
      </plugin>
```

## Configuration properties

The following configuration properties are available:

    descriptionProperty (Default: describe)
      The name of the build property that will contain the output of git
      describe.

    failOutput (Default: unknown)
      String indicating full output if getting version fails

    outputPrefix
      String to prepend to git describe/shorttag output.

    outputSuffix
      String to append to git describe/shorttag output.

    setReactorProjectsProperties (Default: false)
      If true, set the properties on reactor projects.

    extraArguments
      Array of flags to pass to git, wrapped inside `<param>` elements.

### Configuration Example

The plugin might be configured in your pom like so:

```xml
  <configuration>
    <extraArguments>
      <param>--dirty</param>
      <param>--tags</param>
    </extraArguments>
    <setReactorProjectsProperties>true</setReactorProjectsProperties>
  </configuration>
```
