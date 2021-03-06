## Synopsis

A wrapper that allows the use of the [Scalafmt](https://github.com/olafurpg/scalafmt/) formatter in Maven;
The Current Scalafmt version is 0.6.8

## Usage

Add the following snippet to your pom; anything in <parameters> will be
passed through to the CLI as is.

```xml
<plugin>
  <groupId>org.antipathy</groupId>
  <artifactId>mvn-scalafmt</artifactId>
  <version>0.2</version>
  <configuration>
    <parameters>--diff</parameters> <!-- Additional command line arguments-->
    <configLocation>${project.basedir}/path/to/scalafmt.conf</configLocation>
  </configuration>
  <executions>
    <execution>
      <phase>validate</phase>
      <goals>
        <goal>format</goal>
      </goals>
    </execution>
  </executions>
</plugin>
```
