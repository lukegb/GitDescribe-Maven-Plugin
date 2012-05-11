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

Run `mvn help:describe -Dplugin=gitdescribe -Ddetail` to see which
configuration options are available.

