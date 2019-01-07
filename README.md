# Dockit

## Dockit is a markdown document generator for via javadoc.

1. `mvn clean install`

2. pom.xml:

```xml
<plugin>
    <groupId>com.hupubao</groupId>
    <artifactId>dockit-maven-plugin</artifactId>
    <version>1.0.0</version>
    <configuration>
        <scanPackage>cn.lamic.chagoi</scanPackage>
        <templateCharset>UTF-8</templateCharset>
        <singleOutDir>false</singleOutDir>
        <outDir>${project.build.directory}/dockit</outDir>
        <template>${basedir}/src/main/resources/dockit/TEMPLATE.MD</template>
    </configuration>
    <executions>
        <execution>
            <phase>compile</phase>
            <goals>
                <goal>dockit</goal>
            </goals>
        </execution>
    </executions>
</plugin>

```

3. `mvn clean dockit:dockit`

4. You can custom your doc template with [DEFAULT.MD](https://github.com/ysdxz207/dockit/blob/master/src/main/resources/template/DEFAULT.MD)

