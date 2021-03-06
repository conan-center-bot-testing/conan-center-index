# Changelog

### 23-October-2020 - 17:13 CEST

- [feature] ListProfiles: Add 'profiles' to inputs, make it required.
- [feature] Tapaholes: Parameter to accept packages in order from a JSON list.
- [fix] AutomaticMerge: Consider pagination when reading pull-request reviews.
- [job] PopulateProperties: Compute and assign properties to packages-revs and recipe-revs.
- [job] PromotePackages: Copy Conan packages and properties from one repo to another.

### 19-October-2020 - 17:15 CEST

- Updated Conan client to the 1.30.2 version in Windows and Mac agents.

### 14-October-2020 - 17:49 CEST

- [hotfix] Use non greedy regex to capture the pull-request number.

### 10-October-2020 - 21:20 CEST

 - [fix] Wait longer for Artifactory to create new repositories.

### 10-October-2020 - 20:52 CEST

 - [job] TapaholesRepo: use full path to the recipe itself.

### 10-October-2020 - 20:36 CEST

 - [job] BuildSingleReference: assign properties at recipe-revision level

### 10-October-2020 - 15:53 CEST

 - [job] TapaholesRepo: create remote repository for each run.
 - [job] BuildSingleReference: apply environment to every Conan command.

### 09-October-2020 - 23:43 CEST

 - [fix] AutomaticMerge: if the PR cannot be merged (conflicts) go and try the next one.
 - [fix] Use existing TMP folder in Windows.
 - [fix] BuildSingleReference: minor fixes.

### 07-October-2020 - 17:06 CEST

- [fix] Minor fix to AutomaticMerge job (#390)
- [fix] Modify temp folder, it will no longer be the root of the workspace.
- [job] Populate artifact properties from BuildSingleReference job.
- [job] New job to iterate Github repository (and commit) and find packages missing from remote.

### 29-September-2020 - 16:21 CEST

- [feature] Use indexer V2 API.
- [job] Add force parameter to UpdateSearchIndex job to force reindex of packages.
- [job] New UpdateSearchIndexMaster job to reindex (if needed) packages in ConanCenter repository.

### 23-September-2020 - 15:48 CEST

- [job] AutomaticMerge: Approved and changes requested reviews should prevail.

### 21-September-2020 - 17:59 CEST

- [fix] Remove duplicated credentials.
- [job] AutomaticMerge: Block if a team member requested changes on any commit.
- [job] AutomaticMerge: Show pull request number on the summary.

### 21-September-2020 - 10:44 CEST

- Updated Conan client to the 1.29.1 version in Windows and Mac agents.

### 17-September-2020 - 17:42 CEST

- [job] Inspect PRs and merge automatically if approved.
- [job] Build single reference.
- [job] Main tapaholes job: Build single references in correct order.
- [feature] Iterate profiles in a given order (adding tests to check).
- [feature] Add new users to EAP automatically only on Mondays.
- [feature] Distribute jobs taking into account resources.
- [feature] Labels 'Error' and 'Unexpected error' are mutually exclusive.
- [bugfix] Every new node offers a clean workspace (shorter paths).
- [bugfix] Upload packages: upload one first, then the rest to avoid missing files issue.
- [bugfix] Fix 'parallelGroup' when there are more workers than tasks.
- [bugfix] Retry if failure setting the BuildStatus property.
- [fix] Use the actual commit from the 'master' branch to compute diffs.
- [fix] Use environment variables to log into Conan repository.

### 17-August-2020 - 11:20 CEST

- Raise error if zero packages are generated
- Remove "No beta user" label if corresponding check pass
- [engineering] Unify catchs and simplify slackSend function
- [engineering] Pipeline step to create all packages in stages
- [engineering] Pipeline step to compute and reduce 'packageID'
- [engineering] Simplify 'ComputePackageIDs' command

### 12-August-2020 - 10:12 CEST

- Updated Conan client to the 1.28.1 version in Windows and Mac agents.

### 11-August-2020 - 14:19 CEST

- [engineering] Read allowed users from a file.
- [engineering] Check for beta users in all environments.
- [engineering] Set date in issue description for hooks validation job.

### 4-August-2020 - 20:19 CEST

- [engineering] Remove short-paths home after creating packages.

### 31-July-2020 - 23:14 CEST

- [engineering] Use `force` flag to update the ConanCenter metadata.
- [engineering] Remove local packages created after their upload to avoid disk space issues.

### 24-July-2020 - 13:05 CEST

- Renamed Jenkins project from `conan-center-pull-request` to `cci` to improve issues with long workspace paths in Windows agents.

### 24-July-2020 - 12:52 CEST

- Updated Conan client to the 1.27.1 version in Windows and Mac agents.

### 17-July-2020 - 18:54 CEST

- [feature] Allow documentation inside the repository itself in the `docs` folder
- [feature] Add scheduled job to validate recipes using last released hooks
- [feature] Minimize paths used by the CCI library to build packages
- [bugfix] Recover the shortest path for the `CONAN_USER_HOME_SHORT` environment variable
- [engineering] Improve regression testing for pipeline jobs.

### 30-June-2020 - 16:10 CEST

- Add JenkinsPipelineUnit to test the Jenkinsfile
- [bug] Compare keys in maps using actual strings
- Clean workspace after running the job
- Clean workspace for all nodes
- [refact] Promote usage of 'ConanReference'
- [ListProfiles] New job to list profiles
- [fix] Add grabs to all vars
- [Refactor] getTmpDir() util
- [ListProfiles] Optionally use reference to list profiles
- [refact] Some cleaning around build configurations
- [fix] Profiles no longer contain empty [env] and [build_requires] sections
- [fix] Fix checkExportSanity function

### 24-June-2020 - 10:55 CEST
- Updated Conan client to the 1.26.1 version in Windows and Mac agents.

### 18-June-2020 - 18:40 CEST
- Remove short paths limitation in all Windows agents.

### 04-June-2020 - 10:39 CEST
- Add `CONAN_SKIP_BROKEN_SYMLINKS_CHECK=1` in master jobs.

### 02-June-2020 - 13:06 CEST
- Avoid partial rebuilds in master jobs. Added `all_packages_done` property for every reference to track the completion of packages creation.

### 02-June-2020 - 00:02 CEST
- Updated CMake to 3.16.4 in Windows and Mac agents.

### 20-May-2020 - 10:34 CEST
- Updated Conan client to the 1.25.2 version in Windows and Mac agents.

### 14-May-2020 - 15:52 CEST
- Updated Conan client to 1.25.1 version in Windows and Mac agents.

### 13-May-2020 - 09:47 CEST (08e2be6)
- [refact] Simplify around ComputePackageID and CreatePackage
- [refact] No need to pass 'winTmpPath' everywhere
- Move the 'retryIze' call inside the scope of the node (Might improve [#1020](https://github.com/conan-io/conan-center-index/issues/1020))
