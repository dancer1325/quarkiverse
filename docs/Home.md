# Welcome to the Quarkiverse Hub!

* Quarkus
  * 👀crafted -- from -- best Java libraries & standards + extensions👀
  * extensions
    * | beginning, 
      * ALL were accepted | core Quarkus repository
    * | later,
      * NOT ALL accepted
        * Reason:🧠extension's release cadence != core repository's lifecycle🧠
        * -> 💡it's created Quarkivers💡

# What is Quarkiverse

* Quarkus extensions / hosted | Quarkiverse organization
  * 👀are ALLOWED -- through --👀
    * [quarkus generator](http://code.quarkus.io)
    * [quarkus extension catalog](http://extensions.quarkus.io)
    * Quarkus command line tools
      * _Example:_ 
        * `mvn quarkus:list-extensions`
        * `gradle listExtensions`
  * requirements
    * extension 
      * keeps functioning,
      * stays up-to-date
      * cause NO harm

# Why Quarkiverse

* Quarkiverse
  * host Quarkus extension projects / contributed -- by the -- community
    * owned -- by -- EACH project lead
  * advantages of joining
    - Automated & secured publishing of your maven releases | Maven Central
      - == `io.quarkiverse`
    - Automated Cross-testing of your extension -- via -- [Quarkus builds/releases](https://github.com/quarkusio/quarkus-ecosystem-ci) 
    - Consistent formatting & release
    - Quarkus team members can in an emergency help and fix issues
 
* ALTERNATIVES
  * 👀publish a Quarkus extension -- outside of -- Quarkus or Quarkiverse👀
    * STILL can be listed | registry

# Quarkiverse vs Quarkus Platform

* Quarkiverse
  * == "Quarkus" + "universe"
  * == part of the Quarkus ecosystem
  * ⚠️!= Quarkus platform⚠️

* Quarkus platform
  * ⚠️'s requirement⚠️
    * 👀ANY combination of the Quarkus extensions / NO conflict for each other👀
      * thanks to, BETWEEN extensions,
        * coordination + cross testing + dependency version alignment
      * if extensions hosted | Quarkiverse fit this requirement -> can join | Quarkus platform

# Joining Quarkiverse

## Getting an extension onboarded:

* [ChecklistForNewProjects](checklistfornewprojects)

## Documenting your extension

* TODO:
All Quarkiverse extensions can include documentation on http://docs.quarkiverse.io. 
See the [documentation about the documentation](documentingyourextension) for details on how how to document your extension.

## Managing settings on the GitHub repository

Extension maintainers have full control over the repository settings, but be aware that the settings are infrastructure as code, managed with Terraform. 
To change any setting in the repository (give push permissions to anyone, enable a GitHub app, etc.), update the repository's `.tf` file. 
You may notice that, even as an extension maintainer, you have restricted permissions in the GitHub UI. 
This is to reduce the risk of accidents where maintainers make changes which then get overwritten by the next Terraform run.  

## Expectations for Quarkiverse projects 

Quarkiverse projects should follow some [naming conventions](namingconventions) for maven coordinates and package names. 

### Identify Project Maintainer ##

Each project will have a GitHub team, and in here at least one must be listed and active as maintainer. This is the person that will be expected to lead and drive the project.


### Provide mechanism to do cross-testing of named quarkus core and platform versions

All Quarkiverse projects should have a build and test suite that can be parameterized to use specific Quarkus and Platform versions to ensure we can get
early warning of issues of master builds; but also to verify compatibility with maintenance branch/tags.
This is handled by the [ecosystem CI](https://github.com/quarkusio/quarkus-ecosystem-ci).

### Parent POM

All Quarkiverse projects are expected to use [io.quarkiverse:quarkiverse-parent](https://github.com/quarkiverse/quarkiverse-parent) as the parent POM.
This POM contains common project release and artifact publishing configuration.


## LICENSE

The project is expected to be licensed under ASL 2.0.


## Discussions 

[GitHub Discussions](https://docs.github.com/discussions) are disabled by default in Quarkiverse extension repositories.

To avoid spreading information too much and make it hard to figure out where to post we have following default guidelines:

- Development questions should be addressed in the [Mailing List](https://groups.google.com/g/quarkus-dev)
- User questions in [Stack Overflow](https://stackoverflow.com/questions/tagged/quarkus) + the Quarkiverse project tag.

However we can enable it in the repository if the extension maintainer really wants it (open an issue requesting that and ping the `@quarkiverse/quarkiverse-owners` team in the issue). However be aware that Core developers will not follow or be aware of these discussions unless explicitly mentioned.


# Quarkus Extension Development Guides and References

* [how to create a NEW Quarkus extension](https://quarkus.io/guides/building-my-first-extension)
* [guides about writing extensions](https://quarkus.io/guides/#writing-extensions)
