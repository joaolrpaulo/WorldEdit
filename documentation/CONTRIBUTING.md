# Contributing

WorldEdit is open to community contributions. It's also usefull if you need to create an adapter for your software. However, your code must be efficient and tested.

Before cloning the project and start writing code, remember the checklist:

* Have all tabs been replaced into four spaces? Are indentations 4-space wide?
* Have I written proper Javadocs for my public methods? Are the @param and @return fields actually filled out?
* Have I git rebased my pull request to the latest commit of the target branch?
* Have I combined my commits into a reasonably small number (if not one) commit using git rebase?
* Have I made my pull request too large? Pull requests should introduce small sets of changes at a time. Major changes should be discussed with the team prior to starting work.
* Are my commit messages descriptive?

## Branching Model

If you are not used to git, make sure to also be aware of their branching model.

To avoid consecutive merges, commit disorganization and code loss, WorldEdit follows successfull branch model as the figure below.

The develop branch (integration) is the core part where developers are working. Every time a developer needs to create a new feature, they open a new branch, for example `feature/replaceblocks`. After the new feature has been completed, that branch can now be merged back to develop.

Release branches support preparation of a new production release. They allow for last-minute dotting of i’s and crossing t’s. When we finish a release branch, we merge it to master. The changes made on the release branch also need to be merged back into develop, so that future releases also contain these bug fixes.

Hotfix branches are required for critical bugfixes. When completed they need to be merged back into master and develop must also receive those changes.

This is sucessfull git production!

![alt-text](https://github.com/joaolrpaulo/WorldEdit/blob/introduction/documentation/img/gitmodel.png)

## Compiling

The build process uses Gradle, which isn't required to download.

Navigate to WorldEdit folder
`./gradlew clean setupDecompWorkspace`
`./gradlew build`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/compiling.png)

After that you will find:

* The core of WorldEdit in `worldedit-core/build/libs`
* Bukkit adapter in `worldedit-bukkit/build/libs`
* Forge adapter in `worldedit-forge/build/libs`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/compiling3.png)
