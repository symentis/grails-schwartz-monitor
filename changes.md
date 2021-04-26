# Making changes to Schwartz Monitor

* Increment version number in build.gradle and add -SNAPSHOT (whilst working on it)
* Make changes
* Go to one of the test projects, e.g. `cd integration-test-app`
* Run `gradle run`
* Open [quartz monitor page](http://localhost:8080/quartz/list) and make sure jobs are running correctly and the failing job is reported as such
* If everything is ok remove the -SNAPSHOT, commit, tag it (following convention) and push to Sonatype (Maven Central)
* Artifacts are published automatically by GH Actions.
* If you want to publish manually, run `./gradlew publishToSonatype closeAndReleaseSonatypeStagingRepository` (ensure the env vars are set correctly)

