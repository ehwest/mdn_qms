---
repository: "github.com/ehwest/mdn_qms"
title: "README.md"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
approval_date: "2020-10-01"
---

## Purpose

This file contains an overview of the Medical Data Networks LLC Product Development Process.
It overlaps somewhat with the [SOP_0008_Gitflow_Tailoring.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0008_Gitflow_Tailoring.md) under the SOP document folder.

The Product Development Process is by definition the process by which changes to software and services that are used in the T1Pal application and its supporting infrastructure.

The complete Product Developmetn Process is composed of 5 phases.
+ Phase 1:  Research and select specific changes to Standard Operating Procedures to capture in a modified system design.  The deliverable for this phase is the requirements for the change to be made.
+ Phase 2: Develop Software changes by modifying, deleteing, and/or adding code.  There are 6 steps in this phase:
    +  Cut a new feature branch for the change and do development on that feature branch.
    +  When ready, the developer puts the code on a shared developer branch (DEV) for team review and automated testing.
    +  Automated testing happens, triggered by placement of developed code onto the DEV branch.
    +  Technical reviewers sign-off on changes based on test findings.
    +  Changed software is pushed to master branch (per gitflow process)
    +  Cut a new software relase to production using semantic versioning.

+ Phase 3: Maintenance Operations
    +  Review and adjust Fault Management solution (health checks)
    +  perform backups of any impacted dataset.
    +  perform system health checks
    +  validate events detected
    +  fix or roll back software

+ Phase 4:  Release changes to production
    +  follow the release process to deploy code.
    +  if needed, update the SOP
    +  if needed, update the support knowledge base.

+ Phase 5:  Post Market Surveillance
    +  address all of the outstanding bugs reported and assess relative value
    +  address "pain-points" of current and prospective users.
    +  address the features needed to enter new, adjacent markets
    +  address features in the value chain (above and below) to address cost reductions and performance improvements.

General
This is our repository at MDN for general developer/technical documentation that doesn't belong in a specific app/library/service repo.
Table of contents
Here in the docs repository:
•	Code Peer Review Checklist
•	Development Process
•	GitHub Processes
•	External Code Dependency Considerations
•	External Service API Dependency Considerations

Tidepool Code Peer Review Checklists

In order to consistently ensure high quality code, a peer review of all code changes is required. It is recommended that the developer actually perform a code review of their own code before submitting it for peer review. This will hopefully reduce the amount of time and effort spent by the reviewer by catching common issues beforehand.
This document is intended as guidance for engineers. It is not a Standard Operating Procedure (SOP).
Common Checklist
1.	Does the code complete the feature requirements? Does it match the Jira issue?
2.	Is the feature branch up-to-date with the develop branch?
3.	Does the continuous integration build (e.g. Travis, CircleCI) pass? Do any of the non-required continuous integration steps fail? If so, why? Can these be fixed? If not, why not?
4.	If any external dependencies were added:
i.	Review the results of the MDN External Dependency Considerations for each new dependency and sub-dependency.
ii.	Do all of the new dependencies and sub-dependencies use an acceptable license?
iii.	Are the new dependencies and sub-dependencies properly versioned and/or vendored to allow for future repeatable builds?
5.	If any external dependencies were updated:
i.	Was each update explicit?
ii.	Were any updates accidental or unintentional?
6.	Does all new or updated code have a minimum level of test coverage?
7.	Are critical edge cases properly tested?
8.	Is overall test coverage at least the same or improved?
9.	Visually review all new and updated code, with particular focus on the non-test code.
i.	Does it generally follow good industry practices, such as:
a.	Separation of concerns
b.	SOLID
c.	Single responsibility principle - a class should have only a single responsibility (i.e. only changes to one part of the software's specification should be able to affect the specification of the class)
d.	Open/closed principle - software entities should be open for extension, but closed for modification
e.	Liskov substitution principle - objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program
f.	Interface segregation principle - many client-specific interfaces are better than one general-purpose interface
g.	Dependency inversion principle - one should depend upon abstractions, not concretions
h.	DRY - Don't Repeat Yourself
i.	YAGNI - You Ain’t Gonna Need It (did you gold plate it?)
j.	Principle of least privilege - minimum needed to get the job done
ii.	Does it conform to the latest best-practices for that repository, language, and/or framework (e.g. format, lint, import)?
a.	Naming conventions (CamelCase, UPPERCASE, etc.)?
b.	Spaces vs. tabs and indentation, as appropriate for the repository.
iii.	Is it reasonably self-documenting?
a.	Variable names should be descriptive. Use of single-letter variable names are typically only valid for loop index variable names.
iv.	For complex algorithms, is the algorithm documented through more than just the code (i.e. comments)?
v.	Are all returned errors and exceptions checked?
vi.	Are all returned errors and exceptions properly handled? Depending upon the situation this could mean propagating the error to the caller and/or reporting the error to the log.
a.	Are all resources properly disposed even when an error occurs (e.g. files actually closed if there is a failure while reading, temporary files deleted).
vii.	Do all switch statements handle the default case properly?
viii.	Do all for loops correctly manage memory and other resources?
a.	Resources opened within a loop usually need to be confirmed closed in the loop.
b.	Memory allocations within a loop may not be garbage collected until well after the loop completes.
c.	Consider unrolling or breaking up problematic loops.
ix.	If any code was copy-pasted:
a.	Why? Could the code have been reused instead with a little effort?
b.	If not, were any subtle bugs introduced with the copy-paste?
x.	Is it more complicated than it needs to be? Can it be made simpler? Easier to read or understand?
xi.	Does it use framework features wherever possible? No sense in reimplementing standard library features.
xii.	Are there extra features that might get used someday? If so, consider removing the extra, unused code.
xiii.	Are there any functions or methods that are particularly long (e.g. more than 30 lines or so)? Should they be broken down into separate, more focused functions that are easier to understand and test?
xiv.	Is there any newly comment-out code? Any code not being used should be removed. Under certain uncommon circumstances it is okay to leave commented-out code, but there should be detailed documentation before the block that describes why it is commented out and yet still remains in the code.
xv.	Are there any special values or hard-coded values? If so, they should probably be constants or enums, especially if shared across modules/interfaces/API boundaries/etc.
xvi.	If the code relies on external resources (e.g. another service), does it properly handle if the external resource is:
a.	Not available
b.	Timed out
c.	Appears to accept the request, but does not return a response
d.	Returns an unexpected response
xvii.	Is all user input validated before use? (Where user means any input coming from outside of the code, not just a physical person.)
10.	Was any technical debt added?
i.	If so, why? It should be a really, really good reason why it was not addressed
ii.	It should be clearly documented where the tech debt was added.
iii.	A new Jira issue should be created detailing the tech debt and specifically what it will take to remove that debt.
11.	Are there any TODO, FIXME or similar comments? If so, why? TODO is just a form of tech debt, so see above.
12.	Was the Pull Request focused? It is best if the Pull Request is focused to one new feature to make it easier to review.
13.	How many commits are involved in the Pull Request? If there is just one commit for a large number of unrelated changes this may point to lack of focus for the Pull Request. If there are a large number of commits, seriously consider rebasing down to a reasonable number. Strive for one commit per logical unit of work, but a feature may include multiple logical units of work. A logical unit of work is the smallest amount of work that can be completed and still have a functional project.
i.	For example, if I need to do a refactor in order to implement a new feature, it would make sense to have one commit for the refactor (and still have a functioning project), one commit for just the new feature after the refactor, and one overall pull request for both commits.
14.	If there were UX changes, was a design review completed and approved?
15.	Was any pertinent documentation (internal and/or external) properly updated to reflect the code changes?
16.	Is all PII/PHI communication and storage properly encrypted?
17.	Was there any security review?
Specific Checklists
Here are some items to consider that are specific to a particular language and/or framework:
Service Specific Checklist
1.	If there were API or data model changes, was the documentation updated?
2.	If there was a new API added:
i.	Does it require TLS/SSL?
ii.	Does it properly check the request for valid authentication and authorization? Does it properly return an error, if either fail?
3.	Does it belong in that service?
4.	Does the code use local resources (e.g. disk)? If so, will it still work if the next request goes to a different service?
5.	Is the code scalable? Was it tested with more than one node?
6.	Do new database queries correctly use existing indexes? Do they require new indexes? What is the performance impact if a query is used or not?
7.	Do environment specific settings get loaded properly via the standard configuration mechanism for the service?
Golang Specific Checklist
1.	All external dependencies must be vendored using the standard Tidepool Golang dependency management tool (currently go dep).
2.	Best practices for Golang use "early exit on error". Are all errors checked and does the error case return immediately while the success case continues on with the remainder of the function?
3.	Use interfaces wherever possible, but when creating a new struct, return a concrete type, not an interface.
Node.js Specific Checklist
1.	All dependencies must specify an exact version (i.e. 1.2.3). Note that using any other form (e.g. 1.2.x) could yield non-reproducible builds if the lock file is regenerated.
2.	Was a new dependency added? If so, was the yarn.lock file updated to match?
3.	If the yarn.lock file was updated, why? Were the dependency updates reviewed and tested?
React Specific Checklist
1.	Are React packages used/added by this change available in React Native? For both iOS and Android?
iOS Specific Checklist
1.	Use guards to reduce conditional logic in the main body of a function.
2.	Force unwrapping optionals is usually a bad idea. Guards or optional chaining is often a better solution.
3.	Prefer let over var.
4.	Make sure observer registrations are paired with unregistrations
5.	Watch for retain cycles. Use unowned or weak references to break them.
6.	Review for concurrency issues. Data accessed by multiple threads should be protected by a lock
7.	Delegate methods should have the delegating object included in the method signature.
Conclusion
Finally, please consider this document to be evergreen. If you think of additional checklist items that may be useful, please feel free to add them above into the appropriate list and submit as Pull Request.
If you really want to go crazy with a peer review, check out the OWASP Code Review Guide.
Great read on how to keep PR reviews supportive and constructive for both the reviewer and reviewee: Unlearning toxic behaviors in a code review culture.


Tidepool Development Process
Note: in late 2018, Tidepool switched to a new Git branching model that is very similar to GitFlow. The primary differences are the inclusion of required peer reviews for any merge into the master or develop branch and all tags are applied on release and hotfix branches, not the master branch. These relatively minor differences from GitFlow are necessary to accommodate the Tidepool GitHub branch protection requirements.
This document describes the overall development process, including Git branching model, from start to finish. Each specific repository will likely use a slightly modified development process to accommodate language and/or framework requirements. These differences will be highlighted in the repository README.md.
This document assumes you already have a good working knowledge of using Git for software development. In fact, this document does not include all of the Git commands you will need to use during the normal development process. In particular how to add files, remove files, and create commits. If you don't have this knowledge, please learn that first!
For the remainder of this document, all examples assume that the repository name is widgets, the feature branch name is add-tiny-widget, the release version is v1.4.0, and the hotfix version is v1.4.1.
Setup Repository
If starting development on a brand new Tidepool repository, follow the instructions in the Tidepool GitHub Processes document. This will create the repository with the default Tidepool settings, create the develop branch, and configure both the master and develop branch with the required branch protection settings.
Clone the repository to your local machine. For example:
$ mkdir tidepool
$ cd tidepool
$ git clone git@github.com:tidepool-org/widgets.git
Feature Development
Developing a new feature requires following several well-defined steps to ensure an orderly development process.
Create Feature Branch
Create a new feature branch off the latest develop branch. The feature branch name should accurately, but briefly, describe the feature. Use only lowercase ASCII letters, numbers, and dashes (not underscores, periods or any other symbols) in the branch name. For example:
$ git checkout develop
$ git pull
$ git checkout -b add-tiny-widget develop
Develop Feature
Develop the new feature. Add unit tests to fully test the new feature. Ensure all tests pass. Manually test the feature, as necessary. Ensure the new feature matches all done criteria from the related Jira issue. Perform the Tidepool Code Peer Review Checklist process on the completed code to ensure everything it as it should be.
Use standard git operations to add files, remove files, and create commits. Commit the feature code into one or more commits. Each commit should preferably be a single completed unit of work so that, if pushed to origin independently, the Continuous Integration system would build successfully and all tests would pass. Each commit title and description should accurately and completely describe, at a high-level, the changes contained within the commit.
If you prefer to use Git to commit code frequently, even if it is incomplete or does not work, perhaps for "backup" purposes or just because it is the end of the day, please consider rebasing your feature branch and squash code into one commit per completed and tested unit of work. Remember that once commits are merged back into the develop and master branches they are a permanent part of git history for the entire world to see.
On the other hand, do not unnecessarily squash a set of unrelated work into a single commit. This makes a peer review considerably more difficult. So, strive for a balance of focused, but complete commits.
For example, if you need to refactor code before you can implement a new feature, it would make sense to have one commit for the refactor (and still have a functioning project) and one commit for the new feature after the refactor. This will make the review easier and may help isolate whether a newly introduced bug is part of the refactor or the new feature.
Note: If you ever rebase a feature branch that has already been pushed to origin, do not force push the branch (i.e. do not use -f or --force with git push). Instead, create a new feature branch with the same name but append a "dot number" to the end. For example, if the feature branch was add-tiny-widget then any rebased branches would follow the pattern add-tiny-widget.1, add-tiny-widget.2, add-tiny-widget.3, etc. Delete the previous branch both locally and remotely once you have pushed the new rebased branch. Continue working with the new rebased branch.
Merge Latest Develop Branch into Feature Branch
Once you are confident that the feature branch is complete and ready for review, perform a final merge of the develop branch into the feature branch, as it may have changed since you originally created the feature branch. For example:
$ git checkout develop
$ git pull
$ git checkout add-tiny-widget
$ git merge --no-ff develop
Manually resolve any conflicts. Since there may have been automatic or manually resolved conflicts, review any changes and perform a final, full test of the code. All tests must pass.
Push Feature Branch
Now that you are certain the feature branch is complete and contains the latest from the develop branch, push the completed feature branch to origin, if you have not already done so. For example:
$ git push -u origin add-tiny-widget
Deploy Feature Branch (Optional)
Rarely it will be necessary to deploy an in-progress feature branch. Typically this would be to test a specific condition only present when deployed or released. If this occurs, use a feature branch label or tag of the form v<version>-<feature-branch-name>.<number>, where <version> is the version of the active release branch or, if no active release branch is present, the latest deployed version, and <number> starts at 1 and allows for multiple labels or tags. The version should follow Semantic Versioning 2.0.0 rules. A feature branch label or tag of this form is still a valid Semantic Version. Note the v prefix. For example, v1.4.0-add-tiny-widget.1.
Peer Review Feature Branch into Develop Branch
Once you have pushed the completed feature branch to origin and verified that any CI build completes successfully, create a pull request for the peer review. Use either the GitHub Web interface or the command line to create the pull request. For example:
$ open https://github.com/tidepool-org/widgets/pull/new/develop...add-tiny-widget
Ensure the base branch is develop and the compare branch is your final feature branch, particularly if you have rebased one or more times.
Update the title and description, if desired. It may be helpful to add extra notes for the peer reviewer.
In the upper right corner, add one or more Reviewers for this pull request. We no longer specify reviewers via @mentions in the description, but instead use the GitHub Reviewers mechanism.
Generally, only one reviewer is required per pull request. However, if you desire multiple reviewers, then all reviewers must review and approve the pull request. If you are specified as a reviewer, then you must review and approve the pull request even if there are other reviewers. It is not "one of", it is "all". We want to prevent the situation where the reviewers all think someone else is doing the review.
If you aren't sure who should review the pull request, then determine that outside of GitHub (e.g. via Slack) before creating the pull request. We want it to be abundantly clear who is responsible for reviewer the pull request.
For example:
 
Note the pull request reviewer is set to pazaan in the upper right corner.
Click Create pull request. You may wish to notify the reviewer of the pull request via Slack.
Add the pull request to the Jira issue by using a Smart Commit tag. Jira will automatically pick it up.
If you are a requested reviewer, but you will not be able to perform the review in a timely manner, please reach out to the requestor and explain the situation. The requestor may be fine waiting or may decide to choose another reviewer.
The reviewer should use the Tidepool Code Peer Review Checklist to help perform the peer review.
Coordinate with the reviewer to discuss any questions, comments or suggestions. Strive to keep all questions, comments, suggestions, and final decisions in the pull request comment stream so the entire peer review is contained within the pull request itself for future reference. It is acceptable to have in-depth side conversations outside of the pull request (e.g. Slack, email, video chat), but, at a minimum, capture the initial issue, final decision, and its rationale in the pull request comments.
If desired or necessary, update your feature branch and commit any changes. Once complete, follow Push Feature Branch instructions. You may also need to follow Merge Latest Develop Branch into Feature Branch instructions before pushing if the develop branch has recently changed.
Once you and the reviewer are satisfied with the results, the reviewer should approve your pull request and attach the completed Tidepool Code Peer Review Checklist.
For example:
 
Merge Feature Branch into Develop Branch
Once the pull request is approved, the finished feature branch may be merged into the develop branch to definitely add it to the upcoming release.
If the develop branch has changed since you last merged then follow Merge Latest Develop Branch into Feature Branch, Push Feature Branch, and Peer Review Feature Branch instructions again. (The reviewer does not need to complete a full review, but does need to review and approve the final merged code for any issues with possible merge conflicts. This is enforced by the required GitHub branch protection settings.)
Merge the feature branch into the develop branch. For example:
$ git checkout develop
$ git pull
$ git merge --no-ff add-tiny-widget
$ git push origin develop
The --no-ff flag forces the merge to always create a new commit, even if the merge could be performed with a fast-forward. This avoids losing information about the historical existence of the feature branch.
Delete Feature Branch
Assuming the merge and push were successful, delete the feature branch. For example:
$ git branch -d add-tiny-widget
$ git push origin :add-tiny-widget
Release Process
Create Release Branch from Develop Branch
Once all features to be included in a release are merged into the develop branch, create a release branch from the develop branch.
Release branches are named with the release- prefix and the version number of the release. The version number here does not include the v prefix. The version should follow Semantic Versioning 2.0.0 rules. However, normally releases will always use a patch version of 0, with the patch version being reserved for a hotfix. For example, if the previous version was v1.3.1 and the develop branch is "backwards-compatible" with v1.3.1, then the release branch would be named release-1.4.0.
$ git checkout develop
$ git pull
$ git checkout -b release-1.4.0
Perform any repository-specific steps to version and tag the release (e.g. update package.json and create/push the GitHub tag) with a pre-release label. Since this release must be tested and approved by QA and may require one or more changes before it can be deployed, do not initially label or tag the release with its final version number. Instead, use a pre-release label or tag of the form v<version>-release.<number> where <number> starts at 1 and allows for multiple labels or tags. A pre-release label or tag of this form is still a valid Semantic Version. Note the v prefix. For example, v1.4.0-release.1.
Push Release Branch
Push the release branch and any tags to origin. For example:
$ git push -u --tags origin release-1.4.0
Deploy and Test Release Branch
Wait for the official, tagged build artifacts to be available. Deploy the release to a test environment and have QA perform all necessary tests.
Patch Release Branch
If QA finds one or more issues that must be addressed before the release can be deployed, update the code and add commits to the release branch. Increment the <number> for every subsequent pre-release label. For example, v1.4.0-release.2.
Follow Push Release Branch and Deploy and Test Release Branch instructions after every patch.
Finalize Release
Once QA officially approves the release and it is approved for deployment, the release should be finalized.
Perform any repository-specific steps to version and tag the release (e.g. update package.json and create/push the GitHub tag) with its final release label. For example, v1.4.0.
Peer Review Release Branch into Master Branch
Due to the Tidepool GitHub branch protection settings, it is necessary to perform a pull request to approve merging the release branch into the master branch. Use either the GitHub Web interface or the command line to create the pull request. For example:
$ open https://github.com/tidepool-org/platform/pull/new/master...release-1.4.0
Ensure the base branch, compare branch, title, description, and reviewers are correct. The description should note that the pull request is simply to review the merge from the release branch back into the master branch.
Merge Release Branch into Master Branch
Once the pull request is approved, merge the release branch into the master branch. For example:
$ git checkout master
$ git pull
$ git merge --no-ff release-1.4.0
$ git push origin master
Peer Review Release Branch into Develop Branch
Due to the Tidepool GitHub branch protection settings, it is necessary to perform a pull request to approve merging the release branch into the develop branch. Use either the GitHub Web interface or the command line to create the pull request. For example:
$ open https://github.com/tidepool-org/platform/pull/new/develop...release-1.4.0
Ensure the base branch, compare branch, title, description, and reviewers are correct. The description should note that the pull request is simply to review the merge from the release branch back into the develop branch.
Merge Release Branch into Develop Branch
Once the pull request is approved, merge the release branch into the develop branch. For example:
$ git checkout develop
$ git pull
$ git merge --no-ff release-1.4.0
$ git push origin develop
Delete Release Branch
Assuming the previous steps were successful, delete the release branch.
$ git branch -d release-1.4.0
$ git push origin :release-1.4.0
Hotfix Process
Sometimes there is an urgent need to fix a critical issue with production. Since it is not advisable to interrupt normal feature development and release process, the hotfix process should be followed.
Create Hotfix Branch from Master Branch
Create a hotfix branch from the master branch.
Hotfix branches are named with the hotfix- prefix and the version number of the hotfix. The version number here does not include the v prefix. The version should follow Semantic Versioning 2.0.0 rules. Normally, hotfixes will only increment the patch version as this allows any release branches currently in progress to retain their version number. For example, if the previous version was v1.4.0 then this hotfix branch would be named hotfix-1.4.1.
$ git checkout master
$ git pull
$ git checkout -b hotfix-1.4.1
Perform any repository-specific steps to version and tag the hotfix (e.g. update package.json and create/push the GitHub tag) with a pre-hotfix label. Since this hotfix must be tested and approved by QA and may require one or more changes before it can be deployed, do not initially label or tag the hotfix with its final version number. Instead use a pre-hotfix label or tag of the form v<version>-hotfix.<number> where <number> starts at 1 and allows for multiple labels or tags. A pre-hotfix label or tag of this form is still a valid Semantic Version. Note the v prefix. For example, v1.4.1-hotfix.1.
Push Hotfix Branch
Push the hotfix branch and any tags to origin. For example:
$ git push -u --tags origin hotfix-1.4.1
Deploy and Test Hotfix Branch
Wait for the official, tagged build artifacts to be available. Deploy the hotfix to a test environment and have QA perform all necessary tests.
Patch Hotfix Branch
If QA finds one or more issues that must be addressed before the hotfix can be deployed, update the code and add commits to the hotfix branch. Increment the <number> for every subsequent pre-hotfix label. For example, v1.4.1-hotfix.2.
Follow Push Hotfix Branch and Deploy and Test Hotfix Branch instructions after every patch.
Finalize Hotfix
Once QA officially approves the hotfix and it is approved for deployment, the hotfix should be finalized.
Perform any repository-specific steps to version and tag the hotfix (e.g. update package.json and create/push the GitHub tag) with its final hotfix label. For example, v1.4.1.
Peer Review Hotfix Branch into Master Branch
Due to the Tidepool GitHub branch protection settings, it is necessary to perform a pull request to approve merging the hotfix branch into the master branch. Use either the GitHub Web interface or the command line to create the pull request. For example:
$ open https://github.com/tidepool-org/platform/pull/new/master...hotfix-1.4.1
Ensure the base branch, compare branch, title, description, and reviewers are correct. The description should note that the pull request is simply to review the merge from the hotfix branch back into the master branch.
Merge Hotfix Branch into Master Branch
Once the pull request is approved, merge the hotfix branch into the master branch. For example:
$ git checkout master
$ git pull
$ git merge --no-ff hotfix-1.4.1
$ git push origin master
"Target" Release or Develop Branch
If there is active release branch, then use that release branch as the "target" branch in the following few sections. If there is not an active release branch, then use the develop branch as the "target" branch.
Merge "Target" Branch into Hotfix Branch
Note: See "Target" Release or Develop Branch before continuing.
Since the "target" branch may have changes that are not yet included in the hotfix branch, it is necessary to merge those into the hotfix branch before it can be merged back into the "target" branch. This MUST be completed AFTER the hotfix branch is merged into the master branch. For example:
$ git checkout release-1.5.0
$ git pull
$ git checkout hotfix-1.4.1
$ git merge --no-ff release-1.5.0
You may have to manually resolve any conflicts. Since there may have been automatic or manually resolved conflicts, review any changes and perform a final, full test of the code. All tests must pass.
Push Hotfix Branch
Note: See "Target" Release or Develop Branch before continuing.
If there were changes in the "target" branch merged into the hotfix branch then push the hotfix branch to origin. For example:
$ git push -u origin hotfix-1.4.1
Peer Review Hotfix Branch into "Target" Branch
Note: See "Target" Release or Develop Branch before continuing.
Due to the Tidepool GitHub branch protection settings, it is necessary to perform a pull request to approve merging the hotfix branch into the "target" branch. Use either the GitHub Web interface or the command line to create the pull request. For example:
$ open https://github.com/tidepool-org/platform/pull/new/release-1.5.0...hotfix-1.4.1
Ensure the base branch, compare branch, title, description, and reviewers are correct. The description should note that the pull request is simply to review the merge from the hotfix branch back into the "target" branch.
Merge Hotfix Branch into "Target" Branch
Note: See "Target" Release or Develop Branch before continuing.
Once the pull request is approved, merge the hotfix branch into the "target" branch. For example:
$ git checkout release-1.5.0
$ git pull
$ git merge --no-ff hotfix-1.4.1
$ git push origin release-1.5.0
Delete Hotfix Branch
Assuming the previous steps were successful, delete the hotfix branch.
$ git branch -d hotfix-1.4.1
$ git push origin :hotfix-1.4.1


Tidepool External Code Dependency Considerations
If you are thinking about adding a new external code dependency to a Tidepool project, please give serious thought to the following considerations before committing to the dependency. There are few hard-and-fast rules, except perhaps the license requirement, so use your best judgement while taking these considerations into account. When in doubt, pull in another engineer or engineering manager to help with the decision.
This document applies to code. If that code depends on a service API for its operation (e.g. it is a vendor-provided SDK), you may also want to keep in mind the related considerations for service APIs. Those are covered in Tidepool External Service API Dependency Considerations.
You should repeat this process for any additional sub-dependencies that a dependency may pull in.
Common Considerations
1.	What license does the dependency use? The MIT, BSD, and Apache licenses are preferred and may be required depending on how you will be using the dependency. If there is any question, get approval from Howard.
2.	Are there any reasonable alternatives? Spend a few minutes searching for alternatives. If there are alternatives, then use this process with those, too, as a comparison.
3.	How much code is actually going to be used from the dependency? If only a small amount of code compared to the overall size of the dependency, then consider finding an alternative or just implementing it locally. Even consider copy/paste if the license allows for it, but remember to give credit to the original work.
4.	What sub-dependencies does that dependency have? How much extra, unused stuff is coming along for the ride? Apply this process to those sub-dependencies.
5.	What sort of security record does the code or project have? Do they have any outstanding security reports? What is the impact of previously reported security and other types of bugs?
i.	https://cve.mitre.org/cve/search_cve_list.html
ii.	https://www.sourceclear.com/vulnerability-database/search
iii.	https://www.openhub.net/
6.	How active is the community for the dependency?
i.	How many active contributors? Recent turnover? (See event-stream incident)
ii.	What is the frequency and recentness of commits?
iii.	How many open issues are there? What is the impact of these open issues? Do they represent significant problems or just minor problems and feature requests?
iv.	How frequently are issues closed? What is the responsiveness? Why were they closed? Were they actually fixed or were they just closed for lack of progress?
v.	Review GitHub Insights.
7.	How much interest is there from the outside community (e.g. stars, watches, forks)?
i.	Is there any fork that may be more appropriate? Some forks are more active, include additional bug fixes, and are an overall better choice, particularly if work on the primary project has stalled. Repeat this process for any forks that might be viable.
8.	Review the code.
i.	Consider applying all or part of the Tidepool Code Peer Review Checklist against the dependency.
ii.	What does the code look like (readability, understandability, etc.)?
iii.	Does the code conform to any coding standards or best practices for the language?
iv.	What documentation is available?
a.	For external use?
b.	For internal development and maintenance?
v.	What test coverage does the dependency have?
a.	Run the tests. Do the tests pass?
b.	Are they executed automatically on each PR/commit?
vi.	What update strategy does the dependency use for backwards compatibility? Is anything documented? If not, review the change log or actual code changes between previous versions.
vii.	Does it come with build instructions so someone else can build this from scratch, if needed?
9.	How will we "lock" a particular reviewed version of the dependency (and any sub-dependencies) to ensure we get an exact reproducible build (even years later)? Can/should the dependencies be vendored?
10.	Consider the impact of the dependency to our HIPAA compliance requirements
Specific Considerations
Here are some items to consider that are specific to a particular language and/or framework:
Golang Specific Considerations
1.	What version(s) of Golang has the dependency been built and tested against? If it does not explicitly support the latest version the Tidepool repository uses, double check the Golang release notes for that version to see if are any potential conflicts.
2.	Does the dependency use the standard Golang formatting and linting tools?
3.	All external dependencies must be vendored using the standard Tidepool Golang dependency management tool. The reasons for this are:
i.	The go tool chain does not guarantee that a dependency will be available in the future. For example, a developer can delete a repo. Without a store of all published versions, the dependency would disappear.
ii.	The dependencies must be available at build time. Vendoring simply stores those dependencies in the local repo. At present this consists of over 500K lines of Go code. Since space is basically free, this is not a big concern.
Node.js Specific Considerations
1.	Are you using a yarn.lock or a package-lock.json for you repo to ensure that sub-dependencies are locked down?
2.	Only use fixed versions of dependencies, i.e., don’t use version ranges (^,~)
React Specific Considerations
None
iOS Specific Considerations
None
Conclusion
Finally, please consider this document to be evergreen. If you think of additional considerations that may be useful, please feel free to add them above into the appropriate list and submit a Pull Request.


Tidepool External Service API Dependency Considerations
If you are thinking about adding a new external service API dependency to a Tidepool project, please give serious thought to the following considerations before committing to the dependency. There are few hard-and-fast rules, except perhaps the security and privacy requirements, so use your best judgement while taking these considerations into account. When in doubt, pull in another engineer or engineering manager to help with the decision.
This document applies mainly to the service itself, and the APIs it exposes for our use. If that service API is accessed through vendor-provided SDK, you may also want to keep in mind the related considerations for external dependencies as code. Those are covered in Tidepool External Code Dependency Considerations.
You should repeat this process for any additional sub-dependencies that a service API introduces. In other words, other services that are used through calls to service API.
Common Considerations
1.	Are there reasonable alternatives? Including in-house? (build vs. buy/license)
2.	Review the SLA
i.	What is their uptime promise?
ii.	What is their escalation process?
iii.	Is it supported 24/7 globally?
iv.	Do they have an uptime dashboard?
v.	What is their EOL policy for legacy APIs?
3.	Is the API available in all the geographies we need?
i.	Is the performance adequate from other geographies?
ii.	What is their DR plan?
iii.	Do they have automatic failover to another geography?
iv.	If the service stores data persistently, is it subject to GDPR and similar laws?
4.	How will it affect us if the service suffers a prolonged downtime? This could be outside of their control (AWS us-east-1 outage)
5.	Is the API available for different development environments? (dev, stg, prod, …). Are they wholly separate or mixed (e.g. user/account IDs)? Are the non-production environments sufficiently representative of performance etc. of the production environment. Do you have a clear understanding of how they differ?
6.	Is the API rate limited? Does that rate meet our current and forecast needs?
7.	Does the API support bulk operations? Are they needed by our use-cases?
8.	Is there an SDK available in the language(s) we use? Do we need to write our own? Is the wire protocol tolerable (JSON, XML, …)?
9.	Is their code open source? Can you look at it and use the same considerations as Tidepool External Code Dependency Considerations? Is it possible to install it locally and we manage it? Does that make sense?
10.	What plan/consideration should be made if it were to go away overnight? How likely is that?
11.	What does their funding, business model, expected longevity look like?
Security & Privacy Specific Considerations
1.	How is authentication and authorization handled? Whole service vs. per-user?
2.	Is all traffic secured with TLS/SSL? Are their certificates up-to-date?
3.	Will it be handling any PII/PHI data in transit or at rest? Do they comply with HIPAA requirements? Will they sign a BAA, if necessary? If in doubt, consult Howard and Brandon.
4.	What sort of security record does the code or project have? Do they have any outstanding security reports? What is the impact of previously reported security and other types of bugs?
i.	https://cve.mitre.org/cve/search_cve_list.html
ii.	https://www.sourceclear.com/vulnerability-database/search
iii.	https://www.openhub.net/
5.	Do we plan to store any Tidepool or customer data there long-term?
i.	Data encrypted at rest?
ii.	What is the plan for purging (account deletion, GDPR purge requests, …)
Conclusion
Finally, please consider this document to be evergreen. If you think of additional considerations that may be useful, please feel free to add them above into the appropriate list and submit a Pull Request.


Tidepool GitHub Processes
Create Repository
Follow these directions to create a new Tidepool GitHub repository that conforms to the latest Tidepool standards for repository name, license, default branch, and branch protection.
Prepare
Choose a descriptive name for the repository. It must be unique among all other Tidepool GitHub repositories. It must not include tidepool in the repository name, that is implied in the full URL (e.g. github.com/tidepool-org/development). Prefer lowercase and dashes to uppercase and underscore for consistency. Code names are no longer allowed. If you have questions, ask one of the Tidepool GitHub administrators.
Decide whether the repository should have public or private visibility. The repository should be private only if it will contain secrets, security-related matters, third-party proprietary information, or anything else that must not be made public. All other repositories should be public. If you are not sure, ask Howard or Tapani.
Login to GitHub as an Tidepool GitHub administrator. If you aren't a Tidepool GitHub administrator, then you'll need to get one to do the rest.
Create Repository
Browse to https://github.com/organizations/tidepool-org/repositories/new and:
1.	Ensure the Owner is set to tidepool-org.
2.	Enter the Repository name, as chosen above.
3.	Add a Description, if desired, but this can easily be changed later.
4.	Select Public or Private visibility, as chosen above.
5.	Select Initialize this repository with a README.
6.	From the Add .gitignore popup menu choose None.
7.	From the Add a license popup menu choose BSD 2-Clause "Simplified" License.
For example:
 
Click Create repository.
Create Develop Branch
Once the repository is created, create the develop branch so the repository can follow the Tidepool Development Process, which closely models GitFlow.
On the main repository page, click the Branch popup menu, type develop, and click Create branch: 'develop' from 'master'.
For example:
 
Configure Repository Settings
Follow Default Repository Settings instructions below.
Default Repository Settings
Configure Options
Click the Settings icon in the upper-right corner. In the left menu, click Options, and:
1.	Deselect Wikis, Issues, and Projects, unless otherwise required.
2.	Deselect Allow squash merging and Allow rebase merging
For example:
 
Configure Teams
Click the Settings icon in the upper-right corner. In the left menu, click Collaborators & teams and:
1.	Click Add a team, choose Administrators and set permission to Admin
2.	Click Add a team, choose Employees and set permission to Read
3.	Click Add a team, choose the appropriate group (e.g. Engineering, Analytics) and set permission to Write
For example:
 
Configure Default Branch and Branch Protection
Click the Settings icon in the upper-right corner. In the left menu, click Branches.
Select develop as the Default branch and click Update. Click I understand, update the default branch.
For both the master and develop branches, click Add rule to add a Branch protection rule, and:
1.	Enter the branch name (i.e. master or develop)
2.	Select Require pull request reviews before merging
3.	Select Dismiss stale pull request approvals when new commits are pushed
4.	Select Require status checks to pass before merging
5.	Select Require branches to be up to date before merging
6.	Note: If and when you add a Continuous Integration or other connection to this repository, you'll need to come back here and enable all available status checks
7.	Select Include administrators
For example:
 
Click Create. Repeat for both master and develop branches.
For example:
 
---
repository: "github.com/ehwest/mdn_qms"
folder: "PDP_Product_Development_Process"
title: "PDP_phase_3_Maintenance_Operations.md"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
approval_date: "2020-10-01"
---


## Purpose

This document establishes a standard method for completing, identifying, collecting, filing, storing, and dispositioning quality records at Medical Data Networks, LLC (MDN). Quality records are maintained to provide supporting evidence of the conformity, implementation, and effective operation of the QMS.

## References

1. [21 CFR 820](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
2. [FDA](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
3.  [Quality System Regulation](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
4. ISO 13485:2016 Clause 4.2.5

## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this standard operating procedure and for assuring that all employees are trained in its requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this procedure.
---
repository: "github.com/ehwest/mdn_qms"
folder: "PDP_Product_Development_Process"
title: "PDP_phase_4_Release_to_Production.md"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
approval_date: "2020-10-01"
---


## Purpose

This document establishes a standard method for completing, identifying, collecting, filing, storing, and dispositioning quality records at Medical Data Networks, LLC (MDN). Quality records are maintained to provide supporting evidence of the conformity, implementation, and effective operation of the QMS.

## References

1. [21 CFR 820](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
2. [FDA](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
3.  [Quality System Regulation](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
4. ISO 13485:2016 Clause 4.2.5

## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this standard operating procedure and for assuring that all employees are trained in its requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this procedure.
---
repository: "github.com/ehwest/mdn_qms"
folder: "PDP_Product_Development_Process"
title: "PDP_phase_5_Post_Market_Surveillance"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
approval_date: "2020-10-01"
---


## Purpose

This document establishes a standard method for completing, identifying, collecting, filing, storing, and dispositioning quality records at Medical Data Networks, LLC (MDN). Quality records are maintained to provide supporting evidence of the conformity, implementation, and effective operation of the QMS.

## References

1. [21 CFR 820](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
2. [FDA](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
3.  [Quality System Regulation](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
4. ISO 13485:2016 Clause 4.2.5

## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this standard operating procedure and for assuring that all employees are trained in its requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this procedure.
