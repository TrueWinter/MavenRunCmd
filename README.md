# MavenRunCmd

MavenRunCmd is a Maven plugin that allows you to run arbitrary shell commands during the build process.

## Usage

```xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>

<build>
<plugins>
    <plugin>
        <groupId>dev.truewinter</groupId>
        <artifactId>runcmd-maven-plugin</artifactId>
        <!-- Check releases for latest version -->
        <version>1.5</version>
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