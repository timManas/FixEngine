# FixEngine

## Prerequisites

1. Download the QuickFixJ jar file(s) and copy them to folder called resources (screenshot below)
2. Add the jars to each java project by using “Add External Jar” on the build path

## How to Execute

1. Run:
   $ mvn clean package -Dmaven.javadoc.skip=true -DskipTests -PskipBundlePlugin

2. Do NOT delete anything
3. Import project
4. Run:
   $ mvn clean install -Dmaven.javadoc.skip=true -DskipTests -PskipBundlePlugin

5. Run Clean
6. Do a Force Update of SnapShot/Releases on ALL the package

   - Do this by right clicking on top level project
   - Maven -> Update Maven Project
   - Click on checkbox for Force Update of Snapshots/Releases

7. Add JAR using Build Path to each failing project

   - Do this by right clicking on package
   - Build Path > Configure Build Path
   - Go to Tab called Libraries
   - Add External Jar
   - Select quickfix-all-2.3.1.jar

8. Do a clean build again

## Notes

- Commented out the <groupId>org.quickfixj</groupId> from the quickFix-examples.pom file. This will get rid of pom failuressince we deleted the other modules
- Took all the jars from the other modules and placed them in resources folder
