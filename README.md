# Spring Cloud Microservices Monorepo

### Howto create a new service from blank project

1. Unzip blank.zip
2. Rename the folder to new service name (e.g discovery)
3. Rename package and application
4. Update `discovery/pom.xml` and give it new artifactId

```xml
<!-- <artifactId>blank</artifactId> -->
<artifactId>discovery</artifactId>
```

5. Add it to main pom.xml

```xml
    <modules>
        ...
		<module>discovery</module>
	</modules>

	<dependencyManagement>
		<dependencies>
			...
			<dependency>
				<groupId>com.mak.discovery</groupId>
				<artifactId>discovery</artifactId>
			</dependency>
		</dependencies>
	</dependencyManagement>
```
