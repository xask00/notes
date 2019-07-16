# Setting Project name
settings.gradle
 `rootProject.name="testme"`
or directory name

# Multi projects build
in root `settings.gradle`

`include 'sub-project-folder'`

the subproject can still be an independent gradle project, i.e you can go do sub-project and still do ./gradle clean run etc.

What happens when ?

1. ./gradlew clean
2. ./gradlew build (does it execute build in all projects)
3. ./gradle <specific task>

What common settings / configs can be stored in top level project