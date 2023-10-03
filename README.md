# Contributor Roles Notes

## What problem are we trying to solve?

In current practice, repository owners

1. gift authorship to contributors even when the contribution is insignificant, simply because there is no other mechanism to give thanks.
2. omit their contributors entirely, thus giving the impression that only they should be credited with the perceived benefits of the software.

These two problems are easily solved by updating Citation File Format's schema such that the existing key `authors` gets a new branch `contributors`, where `contributors` has the same subschema as `authors`. With the updated format, repository owners would then be able to give credit to their contributors, without being forced to give out authorships in doing so.

- Would fix https://github.com/citation-file-format/citation-file-format/issues/66

A minor thing that still fits within the "citation" use case, as opposed to the "metadata" use case: automatic conversion from CITATION.cff to JATS would not be possible.

## Who or what would consume metadata on roles?

I see the following use cases:

1. Ingest CFF directly
2. Ingest CFF after conversion
3. Human consumption

Some existing direct consumers that I can think of are Zotero, JabRef, GitHub/ruby-cff, Zenodo, and cffconvert. Zotero and JabRef would not make use of a contributor role AFAIK and neither would GitHub/ruby-cff; Zenodo would use the author/contributor differentiation, but Zenodo's (DataCite's) support for contributor roles isn't good when it comes to decribing software contributions, so for our intents and purposes, we can treat Zenodo/DataCite as if they don't have roles at all. `cffconvert` would be able to use contributors, including roles, provided that the target format allows conversion (generally such conversions aren't great).

Maybe in the future, places like LinkedIn, Monsterboard, Indeed and/or headhunters and/or general advertisement agencies (Microsoft/GitHub) can harvest the contributor role metadata from CITATION.cff to build more accurate profiles.

So with that said, is the purpose of differentiating various roles "just" readability for humans, at least for now?

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

|      | Name                                                             | facilitates software | is nested | number of keys | is alive  | has many users |
| ---  | ---                                                              | ---                  | ---       | ---            | ---       | ---            |
| 1.   | [CRediT](tax-credit.md)                                          | meh                  | no        | 14             | yes       | yes            |
| 2.   | [Contribution Ontology](tax-contribution-ontology.md)            | yes                  | yes       | 21 (+68)       | no        | no?            |
| 3.   | [Contributor Role Ontology](tax-contributor-role-ontology.md)    | yes                  | yes       | 32 (+93)       | yes       | no?            |
| 4.   | [Zenodo/DataCite](tax-zenodo-datacite.md)                        | no                   | no        | 21             | yes       | yes            |
| 5.   | [SCoRO](tax-scoro.md)                                            | yes                  | yes       | 4 (+43)        | no?       | no             |
| 6.   | [Habermann](tax-habermann.md)                                    | yes                  | no        | 102            | no        | no             |
| 7.   | [sdruskat.net](tax-sdruskatnet.md)                               | yes                  | no        | 11             | yes       | no             |
| 8.   | [schema.org](tax-schemaorg-codemeta.md)                          | yes                  | no        | 0              | yes       | yes            |
| 9.   | [codemeta](tax-schemaorg-codemeta.md)                            | yes                  | no        | 9              | yes       | maybe          |
| 10.  | [Allcontributors](tax-allcontributors.md)                        | yes                  | no        | 33             | yes       | yes            |
| 11.  | [CrossRef](tax-crossref.md)                                      | no                   | no        | 9              | yes       | yes            |
| 12.  | [ORCID](tax-orcid.md)                                            | meh                  | no        | 25             | yes       | yes            |
| 13.  | [MARC](tax-marc.md)                                              | yes                  | no        | 7              | yes       | yes            |

## Two potential setups

The tables below show how CFF 1.3.0 keys would map onto other taxonomies

1. assuming CFF uses [Allcontributors terminology](tax-allcontributors.md) for its contributor roles, or
1. assuming CFF uses [sdruskat.net terminology with recommendations](tax-sdruskatnet.md).

|     | from Allcontributors | sdruskat.net + recommendations               | to Zenodo/DataCite                                                                            | to CodeMeta 3.0                   | to CRediT                   |
| --- | ---                  | ---                                          | ---                                                                                           | ---                               | ---                         |
| 1.  | `audio`              | `artwork`                                    | <`Other`                                                                                      | no target                         | no target                   |
| 2.  | `a11y`               | `other: accessibility`                       | <`Other`                                                                                      | no target                         | no target                   |
| 3.  | `bug`                | `testing`                                    | <`Other`                                                                                      | no target                         | ~=`Software`?               |
| 4.  | `blog`               | `outreach`                                   | <`Other`                                                                                      | no target                         | no target                   |
| 5.  | `business`           | `funding`? or `other: business development`  | <`Other`                                                                                      | no target                         | no target                   |
| 6.  | `code`               | `development`                                | <`Other`                                                                                      | ==`Coding`                        | ==`Software`                |
| 7.  | `content`            | `other: copywriting, editing`                | <`Other`                                                                                      | no target                         | no target                   |
| 8.  | `data`               | `data`                                       | >~~`DataCollector`~~, >~~`DataCurator`~~, ~=`DataManager`                                     | no target                         | ~=`Data Curation`           |
| 9.  | `doc`                | `documentation`                              | <`Other`                                                                                      | ==`Documentation`                 | no target                   |
| 10. | `design`             | `artwork`                                    | <`Other`                                                                                      | no target, !=`Design`             | !=`Conceptualization`       |
| 11. | `example`            | `documentation`                              | <`Other`                                                                                      | <`Documentation`, <`Support`      | no target                   |
| 12. | `eventOrganizing`    | `outreach`                                   | <`Other`                                                                                      | <`Support`                        | no target                   |
| 13. | `financial`          | `funding`                                    | ==`Sponsor`                                                                                   | no target                         | no target                   |
| 14. | `fundingFinding`     | `funding`                                    | <`Other`                                                                                      | <`Management`                     | ==`Funding acquisition`     |
| 15. | `ideas`              | `conceptualization`                          | <>~~`ProjectLeader`~~, <>~~`ProjectManager`~~, <>~~`WorkPackageLeader`~~, <>~~`Researcher`~~  | <`Architecture`, <`Design`        | ==`Conceptualization`       |
| 16. | `infra`              | `infrastructure`                             | <>~~`HostingInstitution`~~ >~~`DataManager`~~ <`Other`                                        | no target                         | ==`Resources`               |
| 17. | `maintenance`        | `development`                                | <`Other`                                                                                      | ==`Maintenance`                   | <`Software`                 |
| 18. | `mentoring`          | `supervision`?                               | <`ProjectLeader`, <`ProjectManager`, <`Supervisor`, <`WorkPackageLeader`, <`Other`            | no target                         | ~=`Supervision`?            |
| 19. | `platform`           | `development`                                | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 20. | `plugin`             | `development`                                | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 21. | `projectManagement`  | `supervision`                                | ==`ProjectManager`                                                                            | ==`Management`                    | ~=`Project administration`? |
| 22. | `promotion`          | `outreach`                                   | <`Other`                                                                                      | no target                         | no target                   |
| 23. | `question`           | `outreach`                                   | <`Other`                                                                                      | ==`Support`                       | no target                   |
| 24. | `research`           | `conceptualization`? or `other: landscaping` | <`Researcher`                                                                                 | no target                         | no target                   |
| 25. | `review`             | `development`                                | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 26. | `security`           | `other: security`                            | <`Other`                                                                                      | no target                         | no target                   |
| 27. | `tool`               | `development`?                               | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 28. | `translation`        | `outreach`?                                  | <`Other`                                                                                      | <`Coding`                         | <`Software`                 |
| 29. | `test`               | `testing`                                    | <`Other`                                                                                      | ==`Testing`                       | <`Software`                 |
| 30. | `tutorial`           | `outreach`                                   | <`Other`                                                                                      | <`Documentation`, <`Support`      | no target                   |
| 31. | `talk`               | `outreach`                                   | <`Other`                                                                                      | no target                         | no target                   |
| 32. | `userTesting`        | `testing`                                    | <`Other`                                                                                      | <`Testing`?                       | no target                   |
| 33. | `video`              | `artwork`                                    | <`Other`                                                                                      | no target                         | no target                   |


|     | from sdruskat.net with recommendations | to Zenodo/DataCite                                         | to Codemeta 3.0                | to CRediT              |
| --- | ---                                    | ---                                                        | ---                            | ---                    |
| 1.  | `artwork`                              | <`Other`                                                   | no target                      | ~=`Visualization`      |
| 2.  | `conceptualization`                    | <`Other`                                                   | ~=`Design` >~~`Architecture`~~ | ==`Conceptualization`  |
| 3.  | `data`                                 | ~=`DataManager`, >~~`DataCollector`~~, >~~`DataCurator`~~  | no target                      | ~=`Data Curation`      |
| 4.  | `development`                          | <`Other`                                                   | ~=`Coding` >~~`Maintenance`~~  | ~=`Software`           |
| 5.  | `documentation`                        | <`Other`                                                   | ==`Documentation`              | no target              |
| 6.  | `funding`                              | ==`Sponsor`                                                | <>`Management`?                | >`Funding acquisition` |
| 7.  | `infrastructure`                       | >~~`HostingInstitution`~~ >~~`DataManager`~~ <`Other`      | no target                      | ==`Resources`          |
| 8.  | `other`                                | ==`Other`                                                  | no target                      | no target              |
| 9.  | `outreach`                             | <`Other`                                                   | >~~`Support`~~                 | no target              |
| 10. | `supervision`                          | >~~`Supervisor`~~                                          | ~=`Management`                 | ==`Supervision`        |
| 11. | `testing`                              | <`Other`                                                   | ==`Testing`                    | no target              |


Notes:

1. The second table above doesn't need an Allcontributors column, because I can't see any reason to use Allcontributors as a target, only as a source
1. Conversion sources that are bigger concepts than the targets cannot be safely converted, hence I've crossed out the targets.
1. mapping `Allcontributors:design` to `sdruskat.net:conceptualization` would feel like a mismatch; even though a designer conceptualizes something, the (visual) design is not what defines the software project.
1. For CodeMeta, `Role` and `roleName` allow you to write down the exact role name without the need for conversion, but consumption by machines is limited unless people choose to observe the implicit rule about `roleName` being an enum.
1. For schema.org, `Role` and `roleName` allow you to write down the exact role name without the need for conversion, but consumption by machines is limited.
1. for Apalike, Bibtex, Endnote, RIS, contributors are irrelevant.

## About using Allcontributors as a source

1. Concepts such as "design", "architecture", and "conceptualization" are some of the most valued/prestigious categories for researchers, but they are not well represented in Allcontributors terms (`ideas`, ?). See SCoRo's "intellectual" roles for a better list. Maybe the problem goes away if you interpret those "important" roles as author roles?
1. Should we add `roles` to `authors` as well? Given that the `CITATION.cff` is assumed to describe the software (not a paper about the software), the difference between `authors` and `contributors` is only about the substantiveness of their contribution, not about the type of contribution. I guess it also means that a taxonomy enum key for "writing the paper" should go unused.
1. Should `authors` have the same roles as `contributors`? If not, how about using CRediT for `authors` and Allcontributors for `contributors`?

## Loose ends

1. Accountability in Research paper https://www.tandfonline.com/doi/pdf/10.1080/08989621.2020.1779591
1. https://demo.hedgedoc.org/WWA2OwbbSeiVXkTkLSwadA#
