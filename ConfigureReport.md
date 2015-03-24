# Configuring report #

Add this to your pom.xml
```
    <reporting>
        ...
            <plugin>
                <groupId>com.googlecode.maven-overview-plugin</groupId>
                <artifactId>maven-overview-plugin</artifactId>
                <configuration>
                    <width>800</width>
                    <height>800</height>
                    <suppressedScopes/>
                </configuration>
            </plugin>
        ...
    </reporting>
```

For detailed configuration options consult [overview:overview](http://maven-overview-plugin.googlecode.com/svn/site/overview-mojo.html).