# Git-describe Maven plugin

This plugin invokes `git describe` and captures the output in a build variable.

## Configuration

The plugin might be configured in your pom like so:

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

## Configuration properties

The following configuration properties are available:

    descriptionProperty (Default: describe)
      The name of the build property that will contain the output of git
      describe.

    dirty (Default: false)
      If true, pass the `--dirty` flag to git-describe.

    dirtyMark (Default: dirty)
      The <mark> value for the `--dirty` parameter.

    failOutput (Default: unknown)
      String indicating full output if getting version fails

    outputPrefix (Default: git-)
      String to prepend to git describe/shorttag output

    outputSuffix
      String to append to git describe/shorttag output.

    long (Default: false)
      If true, pass the `--long` flag to git-describe.

    setReactorProjectsProperties (Default: false)
      If true, set the properties on reactor projects.



