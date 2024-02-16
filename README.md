# MavenRunCmd

MavenRunCmd is a Maven plugin that allows you to run arbitrary shell commands during the build process.

## Usage

```xml
<pluginRepositories>
    <pluginRepository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </pluginRepository>
</pluginRepositories>

<build>
<plugins>
    <plugin>
        <groupId>dev.truewinter.mavenruncmd</groupId>
        <artifactId>runcmd-maven-plugin</artifactId>
        <version>1.5-SNAPSHOT</version>
        <executions>
            <execution>
                <phase>compile</phase>
                <goals>
                    <goal>build</goal>
                </goals>
                <configuration>
                    <envs>
                        <env>MODE=production</env>
                    </envs>
                    <command>npx webpack</command>
                </configuration>
            </execution>
        </executions>
    </plugin>
</plugins>
</build>
```