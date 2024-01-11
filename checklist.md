# Checklists for Tool quality badging

## Basics - for the FIT coordinator to fill out

These must be met for inclusion; no badge assigned for basic check.

- [ ] Metadata complete, as determined by running against the json schema
- [ ] Links in metadata work
- [ ] A license is included (Where appropriate, [an open source license](https://opensource.org/licenses/)). Commonly used open source licenses include [MIT](https://opensource.org/license/mit/), [GPL 3.0](https://opensource.org/license/gpl-3-0/), and [Apache 2.0](https://opensource.org/license/gpl-3-0/). The [unlicense](https://opensource.org/license/unlicense/) is also an option.
- [ ] For NOAA developed products where the source code is linked, there is a [NOAA disclaimer](https://github.com/nmfs-fish-tools/resources?tab=readme-ov-file#noaa-license) on the readme

# Checklist for reviewers

Thanks for reviewing this tool! Please use the information submitted by the tool authors to fill out the checklist.

If you have any questions, you can ask them directly on this thread by using the `@` in front of their github username in a comment.

## Tool Status

Please check one. Tools with "unacceptable statuses will not be able to be onboarded to FIT.

### Acceptable statuses
- [ ] Stable - The project has reached a stable, usable state. Tools that are stable will be shared on the FIT's main page.
- [ ] Work in Progress - Initial development is in progress, but there has not yet been a stable, usable release suitable for the public. Tools that are works in progress are not ready to feature on the FIT's main page, but will be shared on a separate FIT page.
### Unacceptable statuses
- [ ] Concept - Minimal or no implementation has been done yet, or the repository is only intended to be a limited example, demo, or proof-of-concept. Tools that are concepts will not be shared on the FIT.
- [ ] Abandoned - Initial development has started, but there has not yet been a stable, usable release; the project has been abandoned and the author(s) do not intend on continuing development. Tools that are abandoned will not be shared on the FIT.

## Documentation

Check off all that are complete. A badge will be assigned based upon how many are checked off:

- 0-2 checked = red
- 3-5 checked = orange
- All 6 checked = green

- [ ] Motivation and/or scope of tool. If appropriate, link to examples where the tool has informed science-based decision making.
- [ ] Installation instructions that the reviewer can run. If this is a web app, check this off (Reviewer, please try installing and only check off if install is verified)
- [ ] A getting started example that the reviewer can run (e.g. R vignette; reviewer, please try running this example and only check off if it verified that it can run)
- [ ] How to cite the tool 
- [ ] Documentation of how to use the tool in an appropriate form (e.g., a user manual, function reference: R oxygen documentation, doxygen documentation).
- [ ] Example demonstrating advanced features or functions
- [ ] Web-hosted documentation (e.g., pkgdown site, doxygen site, sphinx, readthedocs)

## Tests

Check off all that are complete. A badge will be assigned based upon how many are checked off

- 0-1 checked = red
- 2-4 checked = orange
- All 5 checked = green

- [ ] Integrated tests have been done (manually or within a testing framework)
- [ ] Unit testing framework used (e.g., testthat, googletest, unittest) that allows running tests with a single command
- [ ] Test coverage acceptable (>40%)
- [ ] Test coverage excellent (>70%)
- [ ] Tests run automatically on code changes or on a schedule (e.g., on GitHub Actions, Travis, Jenkins)
