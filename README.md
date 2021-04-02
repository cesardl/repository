# Own Maven Repository

On current repository:

```bash
mvn install:install-file -DgroupId=<a groupId> -DartifactId=<an artifactId> -Dversion=<a version> -Dfile="<your-path>\<file-nake>.jar" -Dpackaging=jar -DgeneratePom=true -DlocalRepositoryPath=. -DcreateChecksum=true
```

After install, copy the origin from M2_REPO on this GIT project and push.

On Maven pom.xml:

```xml
<repositories>
    <repository>
        <id>GitHub</id>
        <name>My Own Maven Repository on GitHub</name>
        <url>https://raw.githubusercontent.com/cesardl/repository/master/</url>
    </repository>
</repositories>
```
