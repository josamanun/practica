#### Ejemplo de proyecto con maven en el que se integran los siguientes plugins:

* PMD.

* Taglist. Genera un documento HTML con una lista de cosas por hacer, la cual toma etiquetas como TODO y FIXME para generar el documento. Se ejecuta cuando hacemos: mvn site

* Implementada funcionalidad con SLF4J, añadiéndola mediante librería externa y el siguiente plugin en el pom.xml.
```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-install-plugin</artifactId>
    <version>2.4</version>
    <executions>
        <execution>
            <phase>initialize</phase>
            <goals>
                <goal>install-file</goal>
            </goals>
            <configuration>
                <groupId>org.slf4j</groupId>
                <artifactId>slf4j-api</artifactId>
                <version>1.7.21</version>
                <packaging>jar</packaging>
                <file>${basedir}/lib/slf4j-api-1.7.21.jar</file>
            </configuration>
        </execution>
    </executions>
</plugin>
```

Jose Antonio Amaya Nuñez.
