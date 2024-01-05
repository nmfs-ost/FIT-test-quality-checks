# example markdown checklist

## Basics
These must be met for inclusion; no badge assigned for basic check.
- [ ] Metadata complete, including a complete list of authors
- [ ] Links in metadata work
- [ ] A license is included (Where appropriate, an open source license). Commonly used open source licenses include MIT, GPL 3.0, and Apache 2.0. The unlicense is also an option.
- [ ] For NOAA developed products where the source code is linked, there is a disclaimer on the readme (example)

## Status
### Acceptable statuses
- [ ] Stable
### Unacceptable statuses
- [ ] Concept
- [ ] Abandoned
- [ ] Suspended

## Documentation

Check off all that are complete. A badge will be assigned based upon how many are checked off:

- 0-2 checked = red
- 3-5 checked = orange
- All 6 checked = green

- [ ] Motivation and/or scope of tool. If appropriate, link to examples where the tool has informed science-based decision making.
- [ ] Installation instructions that the reviewer can run. If this is a web app, check this off.
- [ ] A getting started One example of use that the reviewer can run (e.g. R vignette)
- [ ] How to cite the tool 
- [ ] Documentation of how to use the tool in an appropriate form (e.g., a user manual, function reference: R oxygen documentation, doxygen documentation).
- [ ] Additional examples of useExample demonstrating advanced features or functions
Web-hosted documentation (e.g., pkgdown site, doxygen site, sphinx, readthedocs)

## Tests

Check off all that are complete. A badge will be assigned based upon how many are checked off

- 0-1 checked = red
- 2-4 checked = orange
- All 5 checked = green

- [ ] Integrated tests have been done (manually or within a testing framework)
- [ ] Unit testing framework used (e.g., testthat, googletest, unittest) that allows running tests with a single command
- [ ] Test coverage acceptable (>40%)
- [ ] Test coverage excellent (>70%)
- [ ]Tests run automatically on code changes or on a schedule (e.g., on GitHub Actions, Travis, Jenkins)
