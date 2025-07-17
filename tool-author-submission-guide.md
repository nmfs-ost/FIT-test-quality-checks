# Tool author submission guide

This is supporting documentation to help tool authors submit their tool to the FIT.

## Meeting the checklist requirements

TODO: Fill this in by checklist item. Provide supporting information for how tool users can go about setting up so that their tool meets the requirements of the checklist. Probably best to go checklist item by checklist item.

### Basics

#### Metadata

To help meet this criteria, fill out all required fields of the onboarding form and follow the instructions. The FIT coordinator will let you know if something isn't working well.

#### Links in metadata work

The FIT coordinator will check that links provided in the submitted onboarding form work, so double checking that the links are correct and up to date before submitting is helpful.

#### License

See complete licensing guidance. In short, if only NOAA FTEs have worked on the tool, an open license is required, and Apache 2.0 or similar licenses are encouraged. If other contributors were included, licensing guidance can be slightly more complicated. Email the FIT service account if you need help figuring out how to license your software.

In general, licenses can be changed, but they require agreement from all who contributed to the software.

#### NOAA Disclaimer

For tools with source code, add a [NOAA disclaimer](https://github.com/nmfs-ost/FIT-resource-files?tab=readme-ov-file#noaa-license) on the README.md of the source code.

### Documentation

#### Background Text

The background text should include a description of the tool and its motivation or scope, as well as the developers or organizations involved. It should also include a link to examples where the tool has informed science-based decision making, if this is appropriate. p

This information can be placed in a README.md file on a source code repository, but it could also be located somewhere else that is easy for users of the software to find.

#### Installation Instructions

Installation instruction should be provided. The tool reviewer must be able to run them and successfully install the software. 

If the software does not require user install, e.g., on a web app, no install instructions need to be provided.

#### A Getting Started Example

A "getting started" example should help orient a beginning user to the software when they are using it for the first time. The example could be embedded in or linked on the README.md of a GitHub repository. It could also be hosted elsewhere, but should be easy to find for users of the software. It should demonstrate how to use the software with a concise example and should not go into advanced use cases. Common examples of 

#### Citation Instructions

Citation intructions provide a way for software users to credit your work. The citation should include a DOI, which provides a permanent link to your software or paper describing it. 

There are several ways to get a DOI for your software. One is to write an academic publication, and then users can cite your publication. Another way is to deposit your sofware in a repository such as Zenodo; Zenodo will create a DOI for your submission which is then citable. Finally, an intermediate way is to submit to a journal like the Journal of Open Source Software, which requires a shortened paper so that it is quick for software authors to put together a submission.

An academic publication takes the most effort and time of these options, but the advantage is that publications are a recognized currency in academic spaces. Zenodo takes the least effort and time, but does not provide users with an additional product for learning about the tool. Finally, the Journal of Open Source software takes less effort than typical academic publications, but still may take just as long to publish, depending on the ability to find reviewers.

#### Tool use documentation

Tool use documentation should instruct the user on how to use the tool. This could be a user guide or function reference, like [roxygen](https://r-pkgs.org/man.html), [doxygen](https://www.doxygen.nl/), or [Sphinx](https://www.sphinx-doc.org/).

For example, for an R package, writing roxygen documentation to generate the [function documentation](https://r-pkgs.org/man.html) is typical. 

#### Advanced features example

An advanced features example provides information on how to run the software for more advanced use cases. If possible, providing a "real" example can be helpful. This should be easy for users to find, for example, linked on the source code readme, if the source code is hosted.

#### Web-hosted Documentation

Web-hosted documentation allows users to more easily browse documentation. Common formats are a pkgdown site or a doxygen site.

For source code that is hosted on GitHub, using GitHub pages to host the documentation may be an option that allows the user to quickly access the web-hosted documentation. 

There are [instructions to host a NOAA-themed pkgdown site](https://nmfs-ost.github.io/noaa-fit-resources/noaa%20resources/NOAA-pkgdown/), which includes a [section on automating the pkgdown rendering](https://nmfs-ost.github.io/noaa-fit-resources/noaa%20resources/NOAA-pkgdown/#automate-your-pkgdown-rendering).

Other options include hosting [Quarto documentation](https://quarto.org/) on the [NMFS Posit Connect server](https://sites.google.com/noaa.gov/nmfs-hq-st-posit-connect/home).

### Tests

#### Integrated Tests

Integrated tests are tests that the software system works together as a whole - for example, an integrated test could be completed in a "Getting Started" example. Ideally, these tests are completed within a testing framework, but sometimes that is not possible. In this case, sharing documentation demonstrating that a manual integration test has been completed is acceptable.

#### Unit Testing Framework

A unit testing framework provides a scaffolding for writing and running tests of your software easily. 

For R package developers, this is likely done using the [testthat](https://testthat.r-lib.org/) R package. A great resource to learn how to set up and use testthat is available in the [Testing Basics Chapter of the R packages book](https://r-pkgs.org/testing-basics.html).

#### Test Coverage

Once a unit testing framework is established, it is possible to calculate test coverage to understand how much of your codebase is being tested.

For R package developers, the covr package provides this functionality.

#### Automated Testing on a continuous integrated service

Continuous integration services provide the ability to run checks and tests automatically, typically at scheduled times or on making changes to code. The increased frequency of running tests makes it easier to catch issues with the code quickly. Options include [GitHub Actions](https://github.com/features/actions) and [Jenkins](https://www.jenkins.io/). GitHub Actions may be the easiest to set up if the codebase is already on GitHub.

For R packages, running [R cmd check](https://r-pkgs.org/R-CMD-check.html) can be helpful way to ensure your R package is ready for users to download, so it is common to set up R cmd check as the primary automated testing check on a continuous integration service. 

There are 2 common ways within NOAA Fisheries to set up R cmd check.

The first approach is using [`usethis::use_github_action(name = "check-standard")`](https://usethis.r-lib.org/reference/use_github_action.html) to generate a GitHub action workflow file that runs R CMD check using the latest version of R on 3 operating systems (Linux, Windows, and Mac) and using the development version of R and the 1 older version of R on Linux only. This is best for users who may want to customize the workflow file or require custom dependencies or options because the user can get the file from r-lib, but then edit it as they please. You will be responsible for maintaining the GitHub Action on your repository, as updates are NOT pushed automatically from `usethis::use_github_action("check-standard")`.

Alternatively, [ghactions4r::use_r_cmd_check()](https://nmfs-ost.github.io/ghactions4r/reference/use_r_cmd_check.html) can be used to generate a "caller" GitHub Action workflow file that calls a reusable workflow. This packaged is maintained by staff within NOAA Fisheries' Office of Science and Technology. This approach is best for users who want to use a standard workflow and do not want to maintain their own action. The benefit of this approach is that the bulk of the workflow is maintained within the ghactions4r package, and users can [open issues in the ghactions4r repository](https://github.com/nmfs-ost/ghactions4r/issues/) to report problems in running the workflow. Changes to the ghactions4r workflow are pushed automatically to the user by modifying the reusable workflow within ghactions4r.


#### Sample Data


Each tool should have at least one sample input dataset along with the application results. Instructions should be given on how a user can run the application with the dataset. The instructions should also include a description of the results and/or a results dataset/plot to compare when running the tests.


#### Usability tests


The user manual should guide the user through navigating the graphical user interface. All UI features should be intuitive and self-documenting. Hover help should be available when the cursor is held over widgets. Whenever the user interacts with the GUI, there should be some feedback to notify the user that the application processed their action.


The developer might investigate using GUI testing applications such as shinytest2 or Selenium. Many are free to use and are available for different languages.
