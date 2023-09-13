# Contributor Roles Notes

## GitHub issues

1. _Align person roles with the OpenRIF Contribution Role Ontology_ https://github.com/citation-file-format/citation-file-format/issues/27
2. _Proposal: Add a contributors field_ https://github.com/citation-file-format/citation-file-format/issues/66
3. _Allow differentiation between authors/contributors_ https://github.com/citation-file-format/citation-file-format/issues/84
4. _Create roles as a simple way to record contribution roles?_ https://github.com/citation-file-format/citation-file-format/issues/112

## Organizations

1. [CASRAI](org-casrai.md)
2. [FORCE16 Attribution Working Group](org-force16-attribution-wg.md)
3. [OpenRIF](org-openrif.md)
4. [Zenodo](org-zenodo.md)

## Ontologies

1. [CRediT](tax-credit.md)
2. [Contribution Ontology](tax-contribution-ontology.md)
3. [Contributor Role Ontology](tax-contributor-role-ontology.md)
4. [Zenodo](tax-zenodo.md)
5. [SCoRO](tax-scoro.md)
6. [Habermann](tax-habermann.md)
7. [sdruskat.net](tax-sdruskatnet.md)
8. [schema.org / codemeta](tax-schemaorg-codemeta.md)
9. [Allcontributors](tax-allcontributors.md)

## Two potential setups

The table below shows what keys would be needed to map a list of conceptual contributions to CFF v1.3.0, 

1. assuming CFF uses [Allcontributors terminology](tax-allcontributors.md) (column 2), or
2. assuming CFF uses [sdruskat.net terminology with recommendations](tax-sdruskatnet.md) (column 3).

|     | Allcontributors concept                                       | CFF == Allcontributors | CFF == sdruskat.net + recommendations        |
| --- | ---                                                           | ---                    | ---                                          |
| 1.  | Audio: ~~Podcasts,~~ background music or sound effects        |  `audio`               | `artwork`                                    |
| 2.  | Accessibility: Reporting or working on accessibility issues   |  `a11y`                | `other: accessibility`                       |
| 3.  | Bug reports                                                   |  `bug`                 | `testing`                                    |
| 4.  | Blogposts                                                     |  `blog`                | `outreach`                                   |
| 5.  | Business Development: People who execute on the business end  |  `business`            | `funding`? or `other: business development`  |
| 6.  | Code                                                          |  `code`                | `development`                                |
| 7.  | Content: e.g. website copy, blog posts are separate           |  `content`             | `other: copywriting, editing`                |
| 8.  | Data                                                          |  `data`                | `data`                                       |
| 9.  | Documentation                                                 |  `doc`                 | `documentation`                              |
| 10. | Design: logo/iconography/visual design/etc.                   |  `design`              | `artwork`                                    |
| 11. | Examples                                                      |  `example`             | `documentation`                              |
| 12. | Event Organizers                                              |  `eventOrganizing`     | `outreach`                                   |
| 13. | Financial Support: for those who provide financial support    |  `financial`           | `funding`                                    |
| 14. | Funding/Grant Finders: People who help find financial support |  `fundingFinding`      | `funding`                                    |
| 15. | Ideas & Planning                                              |  `ideas`               | `conceptualization`                          |
| 16. | Infrastructure: Hosting, Build-Tools, etc.                    |  `infra`               | `infrastructure` fka `resources`             |
| 17. | Maintenance: People who help in maintaining the repo          |  `maintenance`         | `development`                                |
| 18. | Mentoring: People who mentor new contributors                 |  `mentoring`           | `supervision`?                               |
| 19. | Packaging: Porting to support a new platform                  |  `platform`            | `development`                                |
| 20. | Plugin/utility libraries                                      |  `plugin`              | `development`                                |
| 21. | Project Management                                            |  `projectManagement`   | `supervision`                                |
| 22. | Promotion                                                     |  `promotion`           | `outreach`                                   |
| 23. | Answering Questions in Issues, Stack Overflow, etc.           |  `question`            | `outreach`                                   |
| 24. | Research: Literature review                                   |  `research`            | `conceptualization`? or `other: landscaping` |
| 25. | Reviewed Pull Requests                                        |  `review`              | `development`                                |
| 26. | Security: security threats, GDPR, Privacy, etc                |  `security`            | `other: security`                            |
| 27. | Tools                                                         |  `tool`                | `development`?                               |
| 28. | Translation                                                   |  `translation`         | `outreach`?                                  |
| 29. | Tests                                                         |  `test`                | `testing`                                    |
| 30. | Tutorials                                                     |  `tutorial`            | `outreach`                                   |
| 31. | Talks                                                         |  `talk`                | `outreach`                                   |
| 32. | User Testing                                                  |  `userTesting`         | `testing`                                    |
| 33. | Videos                                                        |  `video`               | `artwork`                                    |

Notes:

1. mapping `Allcontributors:design` to `sdruskat.net:conceptualization` would feel like a mismatch; even though a designer conceptualizes something, the (visual) design is not what defines the software project
1. I crossed out podcasts as part of Allcontributors's definition of `audio`, IMO podcasts are `promotion`
1. All categories from sdruskat.net are actually used as targets in the mapping
1. Concepts such as "design", "architecture", and "conceptualization" are some of the most valued/prestigious categories for researchers, but they are not well represented in Allcontributors terms
1. One could use the `allcontributors` bot to do its thing; `CONTRIBUTORS.md` would then be the single source of truth about contributors. Then, use a to-be-created tool to sync `CONTRIBUTORS.md` to `CITATION.cff`, maybe based on GitHub aliases? Insert `contributors[i].alias` in CFF using `CONTRIBUTORS.md` when alias is missing from CFF, but don't add names (requires splitting names into name parts, an unsolvable problem)

### Conversion

- to Apalike: N/A
- to Bibtex: N/A
- to CodeMeta 3.0: `Role` and `roleName` allow you to write down the exact role name without the need for conversion, but consumption by machines is limited unless people choose to observe the implicit rule about `roleName` being an enum.
- to Endnote: N/A
- to Schema.org: `Role` and `roleName` allow you to write down the exact role name without the need for conversion, but consumption by machines is limited.
- to RIS: N/A
- to Zenodo, CodeMeta, CRediT: see below

|     | from Allcontributors                        | to Zenodo                                                  | to CodeMeta 3.0                   | to CRediT      |
| --- | ---                                         | ---                                                        | ---                               | ---            |
| 1.  | `audio`                                     |                                                            | no target                         |                |
| 2.  | `a11y`                                      |                                                            | no target                         |                |
| 3.  | `bug`                                       |                                                            | no target                         |                |
| 4.  | `blog`                                      |                                                            | no target                         |                |
| 5.  | `business`                                  |                                                            | no target                         |                |
| 6.  | `code`                                      |                                                            | `Coding`                          |                |
| 7.  | `content`                                   |                                                            | no target                         |                |
| 8.  | `data`                                      |                                                            | no target                         |                |
| 9.  | `doc`                                       |                                                            | `Documentation`                   |                |
| 10. | `design`                                    |                                                            | no target, !`Design`              |                |
| 11. | `example`                                   |                                                            | <`Documentation`, <`Support`      |                |
| 12. | `eventOrganizing`                           |                                                            | <`Support`                        |                |
| 13. | `financial`                                 |                                                            | no target                         |                |
| 14. | `fundingFinding`                            |                                                            | <`Management`                     |                |
| 15. | `ideas`                                     |                                                            | <`Architecture`, <`Design`        |                |
| 16. | `infra`                                     |                                                            | no target                         |                |
| 17. | `maintenance`                               |                                                            | `Maintenance`                     |                |
| 18. | `mentoring`                                 |                                                            | no target                         |                |
| 19. | `platform`                                  |                                                            | <`Coding`                         |                |
| 20. | `plugin`                                    |                                                            | <`Coding`                         |                |
| 21. | `projectManagement`                         |                                                            | `Management`                      |                |
| 22. | `promotion`                                 |                                                            | no target                         |                |
| 23. | `question`                                  |                                                            | `Support`                         |                |
| 24. | `research`                                  |                                                            | no target                         |                |
| 25. | `review`                                    |                                                            | <`Coding`                         |                |
| 26. | `security`                                  |                                                            | no target                         |                |
| 27. | `tool`                                      |                                                            | <`Coding`                         |                |
| 28. | `translation`                               |                                                            | <`Coding`                         |                |
| 29. | `test`                                      |                                                            | `Testing`                         |                |
| 30. | `tutorial`                                  |                                                            | <`Documentation`, <`Support`      |                |
| 31. | `talk`                                      |                                                            | no target                         |                |
| 32. | `userTesting`                               |                                                            | <`Testing`?                       |                |
| 33. | `video`                                     |                                                            | no target                         |                |
|     | `-----------------`                         | `------------------`                                       | `------------`                    | `------------` |
|     | **from sdruskat.net with recommendations**  | **to Zenodo**                                              | **to Codemeta 3.0**               | **to CRediT**  |
| 1.  | `artwork`                                   | <`Other`                                                   | no target                         |                |
| 2.  | `conceptualization`                         | <`Other`                                                   | >~~`Design`~~ >~~`Architecture`~~ |                |
| 3.  | `data`                                      | >~~`DataManager`~~ >~~`DataCollector`~~ >~~`DataCurator`~~ | no target                         |                |
| 4.  | `development`                               | <`Other`                                                   | >~~`Coding`~~ >~~`Maintenance`~~  |                |
| 5.  | `documentation`                             | <`Other`                                                   | `Documentation`                   |                |
| 6.  | `funding`                                   | >~~`Sponsor`~~                                             | >~~`Management`~~?                |                |
| 7.  | `infrastructure`                            | >~~`HostingInstitution`~~                                  | no target                         |                |
| 8.  | `other`                                     | ==`Other`                                                  | no target                         |                |
| 9.  | `outreach`                                  | <`Other`                                                   | >~~`Support`~~                    |                |
| 10. | `supervision`                               | >~~`Supervisor`~~                                          | `Management`                      |                |
| 11. | `testing`                                   | <`Other`                                                   | `Testing`                         |                |

Notes:

1. Conversion sources that are bigger concepts than the targets cannot be safely converted, hence I've crossed out the targets. For converting from sdruskat.net to Zenodo, that basically leaves only `Other`, which isn't a meaningful. So in our decision making, Zenodo schema terms can be safely ignored -- whatever we come up with maps to Zenodo's `Other` term regardless.

### Preliminary `roles` schema

The file [schema.json](schema.json) describes how to update CFF's JSONSchema file for version 1.3.0. I wrote it for the enum from sdruskat.net + `other` + `artwork`, but it would conceptually be the same for any given `enum`. Combine some online resources to try it out interactively:

1. JSONschema validator [https://www.jsonschemavalidator.net/](https://www.jsonschemavalidator.net/)
2. converting YAML to JSON here [https://onlineyamltools.com/convert-yaml-to-json](https://onlineyamltools.com/convert-yaml-to-json)
3. converting JSON to YAML https://www.json2yaml.com/

```yaml
# a contributor with one role, as string
roles: conceptualization
```

```yaml
# a contributor with one role, as array
roles:
- conceptualization
```

```yaml
# a contributor with multiple roles, as array
roles:
- supervision
- artwork
- conceptualization  # "conceptualization" is a string
```

```yaml
# contributor with multiple roles, as array,
# with free text added to explain
roles:
- supervision
- artwork: drawings
- conceptualization: description of conceptualization
    # "conceptualization" is a key in a dict of length 1
```

```yaml
# contributor with a role that doesn't fit the existing
# role names according to the metadata author
roles:
- other: description of the other activity
```

Notes:

1. Some folks have advocated for having a free text field as CFF contributor role. This would not be useful for downstream usage, consumption by machines, and could hamper automatic validation of the contributor roles. But if we do it like I wrote in the schema file, you can have an element from an `enum`, or a `dict` key with an explanation. In YAML/CFF, this looks pretty clean.
2. The advantage of including an optional description is we can see if people need more roles / how they interpret existing role names.

## Open questions

1. Is this maybe useful https://rollercoaster.shinyapps.io/tenzing/ (Tenzing)
1. https://demo.hedgedoc.org/WWA2OwbbSeiVXkTkLSwadA#
1. if we choose CFF contributor role descriptors that map to CRediT roles, they can be used immeditately with no updates required on the publisher side. This will be a huge benefit for adoption. The easiest way to define CFF contributor roles that map to CRediT roles is to use terms in CFF that are exactly equal to what's used in CRediT.
1. TODO: Look into mapping CRediT roles to Zenodo metadata roles
1. crossref on youtube, homepage https://www.crossref.org/documentation/schema-library/metadata-deposit-schema-5-3-1/
1. schema.org and codemeta have a set of roles as well, (how) can we promote compatibility with them?
1. crossref has its own contributor roles schema: https://www.crossref.org/documentation/schema-library/markup-guide-metadata-segments/contributors/
1. There is talk of supporting CRediT in pkp-lib, https://github.com/pkp/pkp-lib, a library shared by Open Journal Systems (OJS), Open Conference Systems (OCS), Open Monograph Press (OMP), Open Preprint Systems (OPS) and Open Harvester Systems (OHS). https://github.com/pkp/pkp-lib/issues/857
1. contributor atrtriution model as used by the Center for Data to Health: https://contributor-attribution-model.readthedocs.io/en/latest/introduction.html
1. How well do the longer ontologies (Contributor Role Ontology, SCoRO, Habermann) map onto Stephan's ontology, and do we care about the items that do not map well?
1. Stephan's list is high abstraction; many conversion targets are lower-abstraction. This means that conversion is impossible unless you choose to pick one lower abstraction that is covered by CFF's higher abstraction, or you map to all lower abstractions that fit. Both approaches changes the meaning of the original data. For example, CFF may have (only) "Data" role while Zenodo has "DataCollector", "DataCurator", and "DataManager". It is impossible to accurately convert between them despite the fact that they seem so similar.
1. R citation roles https://journal.r-project.org/articles/RJ-2012-009/
1. MARC relator codes https://www.loc.gov/marc/relators/relaterm.html
1. Look into whether datacite defines roles and what they are
