# Contributor Roles Notes

## GitHub issues

1. _Align person roles with the OpenRIF Contribution Role Ontology_ https://github.com/citation-file-format/citation-file-format/issues/27
1. _Proposal: Add a contributors field_ https://github.com/citation-file-format/citation-file-format/issues/66
1. _Allow differentiation between authors/contributors_ https://github.com/citation-file-format/citation-file-format/issues/84
1. _Create roles as a simple way to record contribution roles?_ https://github.com/citation-file-format/citation-file-format/issues/112

## Organizations

1. [CASRAI](org-casrai.md)
1. [FORCE16 Attribution Working Group](org-force16-attribution-wg.md)
1. [OpenRIF](org-openrif.md)
1. [Zenodo](org-zenodo.md)

## Ontologies

|      | Name                                                             | facilitatessoftware | isnested | numberofkeys | isalive   | hasmanyusers |
| ---  | ---                                                              | ---                 | ---      | ---          | ---       | ---          |
| 1.   | [CRediT](tax-credit.md)                                          | yes                 | no       | 14           | yes       | yes          |
| 2.   | [Contribution Ontology](tax-contribution-ontology.md)            | yes                 | yes      | 21 (68)      | no        | no?          |
| 3.   | [Contributor Role Ontology](tax-contributor-role-ontology.md)    | yes                 | yes      | 32 (93)      | yes       | no?          |
| 4.   | [Zenodo/DataCite](tax-zenodo-datacite.md)                        | no                  | no       | 21           | yes       | yes          |
| 5.   | [SCoRO](tax-scoro.md)                                            | yes                 | yes      | 4 (43)       | no?       | no           |
| 6.   | [Habermann](tax-habermann.md)                                    | yes                 | no       | 102          | no        | no           |
| 7.   | [sdruskat.net](tax-sdruskatnet.md)                               | yes                 | no       | 11           | yes       | no           |
| 8.   | [schema.org / codemeta](tax-schemaorg-codemeta.md)               | yes / yes           | no       | 0 / 9        | yes / yes | yes / maybe  |
| 9.   | [Allcontributors](tax-allcontributors.md)                        | yes                 | no       | 33           | yes       | yes          |
| 10.  | [CrossRef](tax-crossref.md)                                      | no                  | no       | 9            | yes       | yes          |

## Two potential setups

The table below shows what keys would be needed to map a list of conceptual contributions to CFF v1.3.0,

1. assuming CFF uses [Allcontributors terminology](tax-allcontributors.md) (column 2), or
1. assuming CFF uses [sdruskat.net terminology with recommendations](tax-sdruskatnet.md) (column 3).

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
| 16. | Infrastructure: Hosting, Build-Tools, etc.                    |  `infra`               | `infrastructure`                             |
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
- to Zenodo/DataCite, CodeMeta, CRediT: see below

|     | from Allcontributors                        | to Zenodo/DataCite                                                                            | to CodeMeta 3.0                   | to CRediT                   |
| --- | ---                                         | ---                                                                                           | ---                               | ---                         |
| 1.  | `audio`                                     | <`Other`                                                                                      | no target                         | no target                   |
| 2.  | `a11y`                                      | <`Other`                                                                                      | no target                         | no target                   |
| 3.  | `bug`                                       | <`Other`                                                                                      | no target                         | ~=`Software`?               |
| 4.  | `blog`                                      | <`Other`                                                                                      | no target                         | no target                   |
| 5.  | `business`                                  | <`Other`                                                                                      | no target                         | no target                   |
| 6.  | `code`                                      | <`Other`                                                                                      | ==`Coding`                        | ==`Software`                |
| 7.  | `content`                                   | <`Other`                                                                                      | no target                         | no target                   |
| 8.  | `data`                                      | >~~`DataCollector`~~, >~~`DataCurator`~~, ~=`DataManager`                                     | no target                         | ~=`Data Curation`           |
| 9.  | `doc`                                       | <`Other`                                                                                      | ==`Documentation`                 | no target                   |
| 10. | `design`                                    | <`Other`                                                                                      | no target, !=`Design`             | !=`Conceptualization`       |
| 11. | `example`                                   | <`Other`                                                                                      | <`Documentation`, <`Support`      | no target                   |
| 12. | `eventOrganizing`                           | <`Other`                                                                                      | <`Support`                        | no target                   |
| 13. | `financial`                                 | ==`Sponsor`                                                                                   | no target                         | no target                   |
| 14. | `fundingFinding`                            | <`Other`                                                                                      | <`Management`                     | ==`Funding acquisition`     |
| 15. | `ideas`                                     | <>~~`ProjectLeader`~~, <>~~`ProjectManager`~~, <>~~`WorkPackageLeader`~~, <>~~`Researcher`~~  | <`Architecture`, <`Design`        | ==`Conceptualization`       |
| 16. | `infra`                                     | <>~~`HostingInstitution`~~ >~~`DataManager`~~ <`Other`                                        | no target                         | ==`Resources`               |
| 17. | `maintenance`                               | <`Other`                                                                                      | ==`Maintenance`                   | <`Software`                 |
| 18. | `mentoring`                                 | <`ProjectLeader`, <`ProjectManager`, <`Supervisor`, <`WorkPackageLeader`, <`Other`            | no target                         | ~=`Supervision`?            |
| 19. | `platform`                                  | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 20. | `plugin`                                    | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 21. | `projectManagement`                         | ==`ProjectManager`                                                                            | ==`Management`                    | ~=`Project administration`? |
| 22. | `promotion`                                 | <`Other`                                                                                      | no target                         | no target                   |
| 23. | `question`                                  | <`Other`                                                                                      | ==`Support`                       | no target                   |
| 24. | `research`                                  | <`Researcher`                                                                                 | no target                         | no target                   |
| 25. | `review`                                    | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 26. | `security`                                  | <`Other`                                                                                      | no target                         | no target                   |
| 27. | `tool`                                      | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 28. | `translation`                               | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 29. | `test`                                      | <`Other`                                                                                      | ==`Testing`                       | <`Software`                 |
| 30. | `tutorial`                                  | <`Other`                                                                                      | <`Documentation`, <`Support`      | no target                   |
| 31. | `talk`                                      | <`Other`                                                                                      | no target                         | no target                   |
| 32. | `userTesting`                               | <`Other`                                                                                      | <`Testing`?                       | no target                   |
| 33. | `video`                                     | <`Other`                                                                                      | no target                         | no target                   |
|     | `-----------------`                         | `------------------`                                                                          | `------------`                    | `------------`              |
|     | **from sdruskat.net with recommendations**  | **to Zenodo/DataCite**                                                                        | **to Codemeta 3.0**               | **to CRediT**               |
| 1.  | `artwork`                                   | <`Other`                                                                                      | no target                         | ~=`Visualization`           |
| 2.  | `conceptualization`                         | <`Other`                                                                                      | ~=`Design` >~~`Architecture`~~    | ==`Conceptualization`       |
| 3.  | `data`                                      | ~=`DataManager`, >~~`DataCollector`~~, >~~`DataCurator`~~                                     | no target                         | ~=`Data Curation`           |
| 4.  | `development`                               | <`Other`                                                                                      | ~=`Coding` >~~`Maintenance`~~     | ~=`Software`                |
| 5.  | `documentation`                             | <`Other`                                                                                      | ==`Documentation`                 | no target                   |
| 6.  | `funding`                                   | ==`Sponsor`                                                                                   | <>`Management`?                   | >`Funding acquisition`      |
| 7.  | `infrastructure`                            | >~~`HostingInstitution`~~ >~~`DataManager`~~ <`Other`                                         | no target                         | ==`Resources`               |
| 8.  | `other`                                     | ==`Other`                                                                                     | no target                         | no target                   |
| 9.  | `outreach`                                  | <`Other`                                                                                      | >~~`Support`~~                    | no target                   |
| 10. | `supervision`                               | >~~`Supervisor`~~                                                                             | ~=`Management`                    | ==`Supervision`             |
| 11. | `testing`                                   | <`Other`                                                                                      | ==`Testing`                       | no target                   |

Notes:

1. Conversion sources that are bigger concepts than the targets cannot be safely converted, hence I've crossed out the targets. For converting from sdruskat.net to Zenodo/DataCite, that basically leaves only `Other`, which isn't a meaningful term. So in our decision making, Zenodo/DataCite schema terms can be safely ignored -- whatever we come up with maps to Zenodo/DataCite's `Other` term regardless.

### Preliminary `roles` schema

The file [schema.json](schema.json) describes how to update CFF's JSONSchema file for version 1.3.0. I wrote it for the [enum from sdruskat.net + recommendations](tax-sdruskatnet.md), but it would conceptually be the same for any given `enum`. Combine some online resources to try it out interactively:

1. JSONschema validator [https://www.jsonschemavalidator.net/](https://www.jsonschemavalidator.net/)
1. converting YAML to JSON here [https://onlineyamltools.com/convert-yaml-to-json](https://onlineyamltools.com/convert-yaml-to-json)
1. converting JSON to YAML https://www.json2yaml.com/

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
1. The advantage of including an optional description is we can see if people need more roles / how they interpret existing role names.

## Loose ends

1. Is this maybe useful https://rollercoaster.shinyapps.io/tenzing/ (Tenzing)
1. https://demo.hedgedoc.org/WWA2OwbbSeiVXkTkLSwadA#
1. if we choose CFF contributor role descriptors that map to CRediT roles, they can be used immeditately with no updates required on the publisher side. This will be a huge benefit for adoption. The easiest way to define CFF contributor roles that map to CRediT roles is to use terms in CFF that are exactly equal to what's used in CRediT.
1. TODO: Look into mapping CRediT roles to Zenodo/DataCite metadata roles
1. contributor attribution model as used by the Center for Data to Health: https://contributor-attribution-model.readthedocs.io/en/latest/introduction.html. Their example uses Contributor Role Ontology: https://contributor-attribution-model.readthedocs.io/en/latest/introduction.html#data-examples
1. How well do the longer ontologies (Contributor Role Ontology, SCoRO, Habermann) map onto Stephan's ontology, and do we care about the items that do not map well?
1. Stephan's list is high abstraction; many conversion targets are lower-abstraction. This means that conversion is impossible unless you choose to pick one lower abstraction that is covered by CFF's higher abstraction, or you map to all lower abstractions that fit. Both approaches changes the meaning of the original data. For example, CFF may have (only) "Data" role while Zenodo/DataCite has "DataCollector", "DataCurator", and "DataManager". It is impossible to accurately convert between them despite the fact that they seem so similar.
1. R citation roles https://journal.r-project.org/articles/RJ-2012-009/ / MARC relator codes https://www.loc.gov/marc/relators/relaterm.html
1. There is talk of supporting CRediT in pkp-lib, https://github.com/pkp/pkp-lib, a library shared by Open Journal Systems (OJS), Open Conference Systems (OCS), Open Monograph Press (OMP), Open Preprint Systems (OPS) and Open Harvester Systems (OHS). https://github.com/pkp/pkp-lib/issues/857
1. Should we add `roles` to `authors` as well? Given that the `CITATION.cff` is assumed to describe the software (not a paper about the software), the difference between `authors` and `contributors` is only about the substantiveness of their contribution, not about the type of contribution. I guess it also means that a taxonomy enum key for "writing the paper" should go unused.
1. Accountability in Research paper https://www.tandfonline.com/doi/pdf/10.1080/08989621.2020.1779591
1. Should authors have the same roles as contributors?


## What problem are we trying to solve?

In current practice, repository owners

1. gift authorship to contributors even when the contribution is insignificant, simply because there is no other mechanism to give thanks.
2. omit their contributors entirely, thus giving the impression that only they should be credited with the perceived benefits of the software.

These two problems are easily solved by updating Citation File Format's schema such that the existing key `authors` gets a new branch `contributors`, where `contributors` has the same subschema as `authors`. With the updated format, repository owners would then be able to give credit to their contributors, without being forced to give out authorships in doing so.

- Fixes https://github.com/citation-file-format/citation-file-format/issues/66

## Who or what would consume metadata on roles?

I see the following use cases:

1. Ingest CFF directly
2. Ingest CFF after conversion
3. Human consumption

Some existing direct consumers that I can think of are Zotero, JabRef, GitHub/ruby-cff, Zenodo, and cffconvert. Zotero and JabRef would not make use of a contributor role AFAIK and neither would GitHub/ruby-cff; Zenodo would use the author/contributor differentiation, but Zenodo's (DataCite's) support for contributor roles isn't good when it comes to decribing software contributions. `cffconvert` would be able to use contributors, including roles, provided that the target format allows conversion (generally such conversions aren't great).

Maybe in the future, places like LinkedIn, Monsterboard, Indeed and/or headhunters and/or general advertisement agencies (Microsoft/GitHub) can harvest the contributor role metadata from CITATION.cff to build more accurate profiles.

So with that said, is the purpose of differentiating various roles "just" readability for humans, at least for now?
