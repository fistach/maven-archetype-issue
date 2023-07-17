# maven-archetype-issue
simplest project allowing to reproduce a maven archetype issue

after 
```
mvn install
mvn archetype:generate -DinteractiveMode=false \
  -DarchetypeGroupId=my.groupId \
  -DarchetypeArtifactId=my-archetype-id \
  -DgroupId=org.test \
  -DartifactId=test \
  -Dversion=0.1 \
  -DarchetypeVersion=1.0-SNAPSHOT
  -DarchetypeCatalog=local
```

the root folder pom.xml contains double end-of-line characters, so lines are spread.

If you remove the <modules> section from the pom.xml, the output pom.xml will have no double end-of-lines.