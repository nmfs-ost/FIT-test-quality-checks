# Tool author submission guide

Thank you for considering your tool for inclusion in the Fisheries Integrated Toolbox (FIT)! This guide is designed to assist tool authors with the submission process and accompanies the reviewer checklist.

Should you find anything requiring clarification or correction, please inform the FIT committee by opening an [issue](https://github.com/nmfs-ost/FIT-onboard-and-update/issues).


## Meeting the checklist requirements

Review of software for inclusion in the FIT is checklist-based. A NOAA internal reviewer will assess your tool for the items on the checklist. The purpose of this process is to offer feedback, enabling you to modify your tool to align with the necessary standards for FIT inclusion.

The FIT committee recognizes that some checklist items may not be widespread practices within NOAA Fisheries, so this guide is provided as support for implementing new practices.

Below are more description and guidance on how to meet items on the reviewer checklist.

### Basics

Everything in the “Basics” section is required.

#### Metadata is complete

To meet this criteria, fill out all required fields of the onboarding form and follow the instructions. The FIT coordinator will let you know if something is missing or needs clarification.

The FIT coordinator will run the metadata against a JSON schema to identify missing information.

#### Links in metadata work
The FIT coordinator will check that the links provided in the submitted onboarding form work. We suggest developers double check that the links they provide are correct before submitting. Note that one working link is required, but not all links are required. There is no need to worry if your software does not have every type of link listed in the onboarding form.

#### A License is included

Please note that this guidance is not legal advice.

For comprehensive licensing guidance, refer to the [complete documentation](https://nmfs-opensci.github.io/GitHub-Guide/#sec-license). Generally, if only NOAA federal employees have contributed to a tool, a permissive open license, such as Apache 2.0, is required. The licensing process can be more complex when other contributors are involved. For assistance with software licensing, contact the FIT service account at fisheries.toolbox@noaa.gov.

While software licenses can be changed, this typically requires agreement from all contributors. It is therefore recommended to establish a license before development begins to simplify the process.


#### NOAA Disclaimer on readme

For tools with source code, add a [NOAA disclaimer](https://github.com/nmfs-ost/FIT-resource-files?tab=readme-ov-file#noaa-license) on the README.md of the source code:

```
## Disclaimer

“This repository is a scientific product and is not official communication of the National Oceanic and Atmospheric Administration, or the United States Department of Commerce. All NOAA GitHub project code
is provided on an ‘as is’ basis and the user assumes responsibility for its use. Any claims against the Department of Commerce or Department of Commerce bureaus stemming from the use of this GitHub project will be governed by all applicable Federal law. Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply
their endorsement, recommendation or favoring by the Department of Commerce. The Department of Commerce seal and logo, or the seal and logo of a DOC bureau, shall not be used in any manner to imply endorsement of any commercial product or activity by DOC or the United States Government.”
```

### Documentation

To be onboarded to the FIT, a tool must meet 4 out of 7 documentation checklist items.


#### Background Text

The background text should include a description of the tool and its motivation or scope, as well as the developers or organizations involved. It should also include a link to examples where the tool has informed science-based decision making, if this is appropriate.

If the source code is linked, this information should be placed in a README.md file on the source code repository. Otherwise, it could also be located somewhere else that is easy for users of the software to find.

#### Installation Instructions

Installation instructions should be provided. The tool reviewer must be able to run them and successfully install the software.

If the software does not require user install, e.g., on a web app, no install instructions need to be provided.

#### A Getting Started Example

For first-time users, a "getting started" example is crucial for orienting them to the software. This concise example, demonstrating basic usage, should be embedded in or linked from the README.md of the source code repository, or otherwise easily discoverable. It should avoid advanced use cases.

#### Citation Instructions

To ensure users properly credit your work, provide citation instructions that include a Digital Object Identifier (DOI). A DOI offers a persistent link to your software or the accompanying paper.
There are three primary methods for obtaining a DOI for your software:
Academic Publication: This involves writing and publishing an academic paper. Users can then cite this publication. While it demands the most effort and time, academic publications are a recognized form of currency in scholarly environments.
Software Repository (e.g., [Zenodo](https://zenodo.org/)): Depositing your software in a repository like Zenodo will generate a citable DOI for your submission. This method requires the least effort and time, but it doesn't offer users an additional resource for learning about the tool.
Open Source Software Journal (e.g., [Journal of Open Source Software](https://joss.theoj.org/)): Journals such as the Journal of Open Source Software require a concise paper, allowing software authors to quickly prepare a submission. This option demands less effort than typical academic publications, though the publication timeline can still be lengthy depending on the review process.

#### Tool use documentation

Tool use documentation, such as a user guide or function reference, should provide instructions on how to use the tool. Examples of such documentation include [roxygen](https://r-pkgs.org/man.html), [doxygen](https://www.doxygen.nl/), and [Sphinx](https://www.sphinx-doc.org/).

#### Advanced features example

An advanced features example provides information on how to run the software for more advanced use cases. If possible, providing a real example can be helpful. The example should be embedded in or linked on the README.md of the source code repository. Otherwise, it should be hosted somewhere easy to find for users of the software.

#### Web-hosted Documentation

Web-hosted documentation allows users to more easily browse documentation. Common formats are a [pkgdown](https://pkgdown.r-lib.org/) site or a [doxygen](https://doxygen.nl/) site.

For source code that is hosted on GitHub, using GitHub pages to host the documentation may be an option that allows the user to quickly access the web-hosted documentation. 

There are [instructions to host a NOAA-themed pkgdown site](https://nmfs-ost.github.io/noaa-fit-resources/noaa%20resources/NOAA-pkgdown/), which includes a [section on automating the pkgdown rendering](https://nmfs-ost.github.io/noaa-fit-resources/noaa%20resources/NOAA-pkgdown/#automate-your-pkgdown-rendering).

Other options include hosting [Quarto documentation](https://quarto.org/) on the [NMFS Posit Connect server](https://sites.google.com/noaa.gov/nmfs-hq-st-posit-connect/home).

### Tests

To be onboarded to the FIT, a tool must meet 4 out of 7 tests checklist items.

#### Integrated Tests

Integrated tests are tests that the software system works together as a whole - for example, an integrated test could be completed in a "Getting Started" example. Ideally, these tests are completed within a testing framework, but sometimes that is not possible. In this case, sharing documentation demonstrating that a manual integration test has been completed is acceptable.

#### Unit Testing Framework

A unit testing framework provides a scaffolding for writing and running tests of your software easily. 

For R package developers, this is likely done using the [testthat](https://testthat.r-lib.org/) R package. A great resource to learn how to set up and use testthat is available in the [Testing Basics Chapter of the R packages book](https://r-pkgs.org/testing-basics.html).

For applications, consider GUI testing toolkits like shinytest2 for Shiny apps or Selenium for web applications.

#### Test Coverage

Once a unit testing framework is established, it is possible to calculate test coverage to understand how much of your codebase is being tested.

For R package developers, the [covr](https://covr.r-lib.org/) package provides this functionality. For Python, [Coverage.py](https://coverage.readthedocs.io/en/7.10.2/) and [pytest-cov](https://pypi.org/project/pytest-cov/) are popular tools. For C++, [gcovr](https://gcovr.com/en/stable/) could be used.

#### Automated Testing on a continuous integrated service

Continuous integration services, such as [GitHub Actions](https://github.com/features/actions) and [Jenkins](https://www.jenkins.io/), automate checks and tests. Running these checks and tests frequently, either on a schedule or when code changes are made, helps to quickly identify and resolve code issues. GitHub Actions is often the simplest to configure if your codebase is already hosted on GitHub.

For R packages, running [R cmd check](https://r-pkgs.org/R-CMD-check.html) can be a helpful way to ensure your R package is ready for users to download, so it is common to set up R cmd check as the primary automated testing check on a continuous integration service. 

There are 2 common ways within NOAA Fisheries to set up R cmd check.

The first approach is using [`usethis::use_github_action(name = "check-standard")`](https://usethis.r-lib.org/reference/use_github_action.html) to generate a GitHub action workflow file that runs R CMD check using the latest version of R on 3 operating systems (Linux, Windows, and Mac) and using the development version of R and the 1 older version of R on Linux only. This approach is best for users who may want to customize the workflow file or require custom dependencies or options because the user can edit the GitHub Actions file as they please. You will be responsible for maintaining the GitHub Action on your repository, as updates are NOT pushed automatically from `usethis::use_github_action("check-standard")`.

Alternatively, [ghactions4r::use_r_cmd_check()](https://nmfs-ost.github.io/ghactions4r/reference/use_r_cmd_check.html) can be used to generate a "caller" GitHub Action workflow file that calls a reusable workflow. This package is maintained by staff within NOAA Fisheries' Office of Science and Technology. This approach is best for users who want to use a standard workflow and do not want to maintain their own action. The benefit of this approach is that the bulk of the workflow is maintained within the ghactions4r package, and users can [open issues in the ghactions4r repository](https://github.com/nmfs-ost/ghactions4r/issues/) to report problems in running the workflow. Changes to the ghactions4r workflow are pushed automatically to the user by modifying the reusable workflow within ghactions4r.


#### Sample Data

For each tool, provide at least one sample input dataset and the corresponding application results. Include instructions on how to run the application with the dataset, a description of the results and/or a results dataset or plot for comparison.


#### Usability tests

Provide information about usability tests that have been conducted, what was found, and what changes were made as the result of the usability tests.

When testing an app for usability, users should consider the following best practices:
The user manual should provide clear guidance on navigating the graphical user interface (GUI).
All UI features should be intuitive and self-explanatory.
Hover-over help should be available for all widgets.
The application should provide feedback to the user after every interaction with the GUI, confirming that the action has been processed.


