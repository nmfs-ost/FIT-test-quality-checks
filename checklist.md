# Checklists for Tool quality badging

## Basics - for the FIT coordinator to fill out

These must be met for inclusion; no badge assigned for basic check.

- [ ] Metadata is complete, as determined by running against the json schema
- [ ] Links in metadata work
- [ ] A license is included (where appropriate, [an open source license](https://opensource.org/licenses/)).
- [ ] For NOAA-developed products where the source code is linked, there is a [NOAA disclaimer](https://github.com/nmfs-fish-tools/resources?tab=readme-ov-file#noaa-license) on the readme of the source code.
- [ ] After review: Add FIT badges to metadata based on reviewer's work.

# Checklist for reviewers

Thanks for reviewing this tool! Please use the information submitted by the tool authors to complete the checklist.

If you have any questions, you can ask them directly on this thread by using the `@` in front of their github username in a comment.

## Documentation

Check off all items that are complete. A badge will be assigned based upon the number of items checked off:

- 0-2 checked = red
- 3-6 checked = orange
- All 7 checked = green

- [ ] Background text includes a description of the tool and its motivation and/or scope. If appropriate, it also includes a link to examples where the tool has informed science-based decision making.
- [ ] Installation instructions are provided that the reviewer can run. Reviewer, please attempt installation and only check this off if install is verified. If this is a web app or other software type that does not require installation, check this off.
- [ ] A getting started example (e.g., R vignette) is provided that the reviewer can run. Reviewer, attempt to run this example and only check this off if verified to run.
- [ ] Instructions on how to cite the tool are included.
- [ ] Documentation on how to use the tool in an appropriate form (e.g., a user manual, or function reference: roxygen, doxygen, Sphinx).
- [ ] An example demonstrating advanced features or functions is included.
- [ ] Web-hosted documentation is available (e.g., pkgdown site, doxygen site, readthedocs).

## Tests

Check off all items that are complete. A badge will be assigned based on the number of items checked off:

- 0-1 checked = red
- 2-4 checked = orange
- 5-7 checked = green

- [ ] [Integrated tests](https://en.wikipedia.org/wiki/Integration_testing) have been conducted (manually or within a testing framework).
- [ ] A unit testing framework (e.g., testthat, googletest, unittest) is used that allows running tests with a single command.
- [ ] Test coverage is acceptable (>40%).
- [ ] Test coverage is excellent (>70%).
- [ ] Tests set up on a continuous integration service to run automatically on code changes or on a schedule (e.g., on GitHub Actions, Travis, Jenkins).
- [ ] Sample data provided to validate functionality.
- [ ] Usability tests have been conducted and results are provided.
