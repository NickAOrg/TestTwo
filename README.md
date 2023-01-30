<!-- This is a comment in md (Markdown) format, it will not be visible to the end user -->

<!-- Update the below line with your artifact name -->
# Push Bundles to GitHub

<!-- Leave TOC intact unless you've added or removed headers -->
## Table of Contents

* [Overview](#overview)
* [Installation Prerequisites](#installation-prerequisites)
* [Requirements](#requirements)
* [Features](#features)
* [How to Install](#how-to-install)
* [How to Run](#how-to-run)

## Overview

<!-- Write a few sentences about the artifact and explain the use case(s) -->
<!-- Ex.: The Migration Wizard enables IAP users to conveniently move their automation use cases between different IAP environments -->
<!-- (e.g. from Dev to Pre-Production or from Lab to Production). -->

<!-- Workflow(s) Image Placeholder - TO BE ADDED DIRECTLY TO GitHub -->
<!-- REPLACE COMMENT BELOW WITH IMAGE OF YOUR MAIN WORKFLOW -->
<!-- <!--  -->
The **Push Bundles to GitHub** pre-built takes an Admin Essentials installed pre-built and creates a new project in GitHub using the up-to-date pre-built bundle.
If the project and branch already exists in the specified GitHub group, it will create a new branch and open a pull request in GitHub with any changes made in the lab environment. 

<table><tr><td>
  <img src="https://gitlab.com/itentialopensource/pre-built-automations/push-bundle-to-github/-/raw/release/2021.2/images/workflow.png" alt="workflow" width="800px">
</td></tr></table>
<!-- REPLACE COMMENT ABOVE WITH IMAGE OF YOUR MAIN WORKFLOW -->

<!-- ADD ESTIMATED RUN TIME HERE -->
<!-- e.g. Estimated Run Time: 34 min. -->

## Installation Prerequisites

Users must satisfy the following pre-requisites:

<!-- Include any other required apps or adapters in this list -->
<!-- Ex.: EC2 Adapter -->
* Itential Automation Platform
  * `^2021.2`
* App-Artifacts
  * `6.1.16-2021.1.2`
* [GitHub Adapter](https://gitlab.com/itentialopensource/adapters/devops-netops/adapter-github)


## Requirements

This artifact requires the following:

<!-- Unordered list highlighting the requirements of the artifact -->
<!-- EXAMPLE -->
<!-- * cisco ios device -->
* Artifact installed in Admin Essentials
* GitHub Organization Name

## Features

The main benefits and features of the artifact are outlined below.

<!-- Unordered list highlighting the most exciting features of the artifact -->
<!-- EXAMPLE -->
<!-- * Automatically checks for device type -->
<!-- * Displays dry-run to user (asking for confirmation) prior to pushing config to the device -->
<!-- * Verifies downloaded file integrity (using md5), will try to download again if failed -->
* Automatically create repo and branch.
* Automatically create Pull Request when repo and branch exist.
* Allows user to perform rediscovery of an installed artifact (where new components were added).
* Adds the current IAP user whoami username to the Pull Request description for the Pull Request reviewer.
* Auto artifact.json generator script
* Helps to handle "Artifact-As-Code" with version control, PR, and code-promotion procedures.


<!-- ## Future Enhancements -->

<!-- OPTIONAL - Mention if the artifact will be enhanced with additional features on the road map -->
<!-- Ex.: This artifact would support Cisco XR and F5 devices -->

## How to Install

To install this pre-built:

* Verify you are running a supported version of the Itential Automation Platform (IAP) as listed above in the [Requirements](#requirements) section. 
* The artifact can be installed from within App-Admin_Essential. Simply search for the name of your desired artifact and click the install button (as shown below).

<!-- REPLACE BELOW WITH IMAGE OF YOUR PUBLISHED ARTIFACT -->
<!-- <!-- -->
<table><tr><td>
  <img src="https://gitlab.com/itentialopensource/pre-built-automations/push-bundle-to-github/-/raw/release/2021.2/images/install.png" alt="install" width="600px">
</td></tr></table>

<!-- REPLACE ABOVE WITH IMAGE OF YOUR PUBLISHED ARTIFACT -->

<!-- OPTIONAL - Explain if external components are required outside of IAP -->
<!-- Ex.: The Ansible roles required for this artifact can be found in the repository located at https://GitHub.com/itentialopensource/pre-built-automations/hello-world -->

## How to Run

Use the following to run the artifact:

<!-- Explain the main entrypoint(s) for this artifact: Automation Catalog item, Workflow, Postman, etc. -->

1. In Automation Catalog, find the **Push Bundles to GitHub** entry.
2. Fill out the form (as shown below) with the appropriate values.
3. Continue with all manual tasks in the workflow.

<table><tr><td>
  <img src="https://gitlab.com/itentialopensource/pre-built-automations/push-bundle-to-github/-/raw/release/2021.2/images/form.png" alt="form" width="600px">
</td></tr></table>

Form Inputs (look for above screenshot for example inputs)
1. Adapter Name - Adapter name configured with user token
2. GitHub Project Name - Project name in GitHub to Update/Create
3. GitHub Organization Name - GitHub organization name to push repository
4. Re-discover - Perform re-discover
5. Artifact - name of the installed bundle to push onto remote repo
6. PR Type - Type of PR (patch/minor/major)
7. Commit Message -  Commit message to add for commit tasks
8. Target Branch - Traget branch to set for PR
