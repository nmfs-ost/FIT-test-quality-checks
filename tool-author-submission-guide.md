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

The background text should include a description of the tool and its motivation or scope. It should also include a link to examples where the tool has informed science-based decision making, if this is appropriate.

This information can be placed in a README.md file on a source code repository, but it could also be located somewhere else that is easy for users of the software to find.

#### Installation Instructions

Installation instruction should be provided. The tool reviewer must be able to run them and successfully install the software.

If the software does not require user install, e.g., on a web app, no install instructions need to be provided.

#### A Getting Started Example

A "getting started" example should help orient a beginning user to the software when they are using it for the first time. The example could be embedded in or linked on the README.md of a GitHub repository. It could also be hosted elsewhere, but should be easy to find for users of the software. It should demonstrate how to use the software with a concise example and should not go into advanced use cases.

#### Citation Instructions

Citation intructions provide a way for software users to credit your work. The citation should include a DOI, which provides a permanent link to your software or paper describing it. 

There are several ways to get a DOI for your software. One is to write an academic publication, and then users can cite your publication. Another way is to deposit your sofware in a repository such as Zenodo; Zenodo will create a DOI for your submission which is then citable. Finally, an intermediate way is to submit to a journal like the Journal of Open Source Software, which requires a shortened paper so that it is quick for software authors to put together a submission.

An academic publication takes the most effort and time of these options, but the advantage is that publications are a recognized currency in academic spaces. Zenodo takes the least effort and time, but does not provide users with an additional product for learning about the tool. Finally, the Journal of Open Source software takes less effort than typical academic publications, but still may take just as long to publish, depending on the ability to find reviewers.

#### Tool use documentation

Tool use documentation should instruct the user on how to use the tool. This could be a user guide or function reference, like roxygen, doxygen, or Sphinx.

For example, for an R package, writing roxygen documentation to generate the [function documentation](https://r-pkgs.org/man.html) is typical. 

#### Advanced features example

An advanced features example provides information on how to run the software for more advanced use cases. If possible, providing a "real" example can be helpful. This should be easy for users to find, for example, linked on the source code readme, if the source code is hosted.

#### Web-hosted Documentation

Web-hosted documentation allows users to more easily browse documentation. Common formats are a pkgdown site, a doxygen site, or readthedocs site.

For source code that is hosted on GitHub, using GitHub pages to host the documentation may be an option that allows the user to quickly access the web-hosted documentation. 

There are [instructions to host a NOAA-themed pkgdown site](https://nmfs-ost.github.io/noaa-fit-resources/noaa%20resources/NOAA-pkgdown/), which includes a [section on automating the pkgdown rendering](https://nmfs-ost.github.io/noaa-fit-resources/noaa%20resources/NOAA-pkgdown/#automate-your-pkgdown-rendering).


Other options include hosting Quarto documentation on the [NMFS Posit Connect server](https://sites.google.com/noaa.gov/nmfs-hq-st-posit-connect/home).




### Tests

#### Integrated Tests

#### Unit Testing Framework

#### Test Coverage

#### Automated Testing on a continuous integrated service

#### Sample Data

#### Usability tests