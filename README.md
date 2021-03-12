> Starts with 10.0.0 due to historical reasons.

# Usage

To use this pom.xml as a parent please overwrite the `scm connection` setting with the proper URL for your organization.  
For example:
```
<scm>
    <connection>scm:git:https://github.com/mig-frankfurt/</connection>
</scm>
```
Insert the `scm connection` setting into the `<project>` tag of your pom.xml.

If you have an organization with multiple projects that all require the same `scm connection` setting and maybe also share other settings please create a new parent pom.xml for them.  
For example see https://github.com/mig-frankfurt/mdr.maven.spring

# Content

This pom.xml contains distribution management for the MIG nexus repository and a profile that ensures correct code style (Google Java Codestyle) and proper dependency management.  
Proper dependency management implies the following:
* Declared, unused dependencies must be removed.
* Undeclared, used dependencies must be added.
* Snapshot dependencies are not allowed if the project is in a non-snapshot version.
