# Dependency-Track Jenkins Plugin - Changelog

## Unreleased

## v3.1.0 - 2021-02-08
### ⭐ New Features
- allow to specify an alternative URL for the Dependency-Track Frontend (fixes [#22](https://github.com/jenkinsci/dependency-track-plugin/issues/22))
- added links to npm security advisories

### 🐞 Bugs Fixed
- verify that `projectId` is set when auto create projects is not enabled

## v3.0.2 - 2020-12-09
### 🐞 Bugs Fixed
- link to project page not working for Dependency-Track older than v3.8, part 2 (previous fix was incomplete)

## v3.0.1 - 2020-12-08
### 🐞 Bugs Fixed
- link to project page not working for Dependency-Track older than v3.8 (fixes [#17](https://github.com/jenkinsci/dependency-track-plugin/issues/17))
- Report does not render correctly in Firefox (fixes [#18](https://github.com/jenkinsci/dependency-track-plugin/issues/18))

## v3.0.0 - 2020-11-30
### ⚠ Breaking
- Internet Explorer 11 is not supported anymore
- minimum required Jenkins version is now 2.249.2
- configuration is not compatible with previous versions
  - due to internal changes
  - **API key is now of type "Secret Text" credential**

### ⭐ New Features
- allow to override global values for Dependency-Track URL, API key and "Auto Create Projects" in job definition (fixes [JENKINS-55926](https://issues.jenkins.io/browse/JENKINS-55926))
- support multiple invocations in a build run (fixes [JENKINS-55926](https://issues.jenkins.io/browse/JENKINS-55926)).

  **please note**: Only the result of the last invocation using `synchronous=true` will contribute to the result report page and the history on the job page.

- allow to specify connect and response timeouts
- re-designed result report page
- added link on the sidebar to Dependency-Track project page for each build (*only for new builds*, fixes [JENKINS-55627](https://issues.jenkins.io/browse/JENKINS-55627))
- support dark theme of Jenkins 2.249
- [JENKINS-57697](https://issues.jenkins.io/browse/JENKINS-57697): more detailed error logging
- API key is now a "Secret Text" credential
- list of projects in job configuration page is now sorted and includes only active projects

### 🐞 Bugs Fixed
- unable to use `projectName` and `projectVersion` instead of `projectId` in classic job types
- sorting of column "Severity" in result report table was broken
- corrected the help information for global setting "Polling Timeout"

## v2.3.0 - 2020-05-21
### ⚠ Breaking
- removed `artifactType` parameter
- minimum required Jenkins version is now 2.222.3

### ⭐ New Features
-  [JENKINS-57640](https://issues.jenkins.io/browse/JENKINS-57640): Support Configuration As Code
