# test-quality-checks
Test out the tool quality checks.

See the .github/workflows folder to preview the checklists.

## Process for review

1. Author submits tool using the "quality review checklist" issue under https://github.com/nmfs-ost/FIT-test-quality-checks/issues
2. FIT coordinator generates the basics checklist using `/generate-basics-checklist` in an issue comment and completes it.
3. Once basics is completed, FIT coordinator identifies a reviewer.
4. Once a reviewer is identified, the FIT coordinators uses `/generate-reviewer-instructions @reviewer-github-name` to generate instructions for the reviewer.
5. The reviewer generates their checklist using `/generate-reviewer-checklist` and completes it. They can ask questions to the author as needed.
6. Once the tool is accepted, the FIT coordinator generates the post-acceptance checklist using `/generate-post-acceptance-checklist` and completes it.
7. Once the post-acceptance checklist is complete and the author is satisfied with how the page looks on the FIT, the software is included on the FIT production website.

> Note: Use `/list-commands` to see command options available for use.

### Reviewing existing tools (section under construction)

These software already have metadata in the FIT. What needs to happen is:
1. Author reviews metadata and changes it as needed.
2. Author adds additional info needed for the peer review process, should not need to re-enter existing metadata.
3. Complete 2-7 for the software tool.


## disclaimer

“The United States Department of Commerce (DOC) GitHub project code is provided on an ‘as is’ basis and the user assumes responsibility for its use. DOC has relinquished control of the information and no longer has responsibility to protect the integrity, confidentiality, or availability of the information. Any claims against the Department of Commerce stemming from the use of its GitHub project will be governed by all applicable Federal law. Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by the Department of Commerce. The Department of Commerce seal and logo, or the seal and logo of a DOC bureau, shall not be used in any manner to imply endorsement of any commercial product or activity by DOC or the United States Government.”
