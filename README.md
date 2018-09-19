# setbaseuri-maven-plugin

This plugin adds the `project.baseUri` to project properties. 
This property **should** be defined by lmaven, but isn't. So let's add a plugin to do it.

Sample :

```xml
    <build>
      <plugins>
        <plugin>
          <groupId>top.marchand.maven</groupId>
          <artifactId>setbaseuri-maven-plugin</artifactId>
          <version>1.0.0</version>
          <executions>
            <execution>
              <phase>initialize</phase>
              <goals><goal>seturi</goal></goals>
            </execution>
          </executions>
        </plugin>
      </plugins>
    </build>
```

Then, in a filtered resource, you can use `${poroject.baseUri}`, it will be substitued with
a URI form of project directory : `file:/Users/cmarchand/devel/project` for me.
