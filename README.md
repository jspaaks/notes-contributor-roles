# Contributor Roles Notes

GitHub issues:

1. _Align person roles with the OpenRIF Contribution Role Ontology_ https://github.com/citation-file-format/citation-file-format/issues/27
1. _Proposal: Add a contributors field_ https://github.com/citation-file-format/citation-file-format/issues/66
1. _Allow differentiation between authors/contributors_ https://github.com/citation-file-format/citation-file-format/issues/84
1. _Create roles as a simple way to record contribution roles?_ https://github.com/citation-file-format/citation-file-format/issues/112

---

## Organizations

### CASRAI

CASRAI is short for Consortium for Advancing Standards in Research Administration Information. They are "a consortium of research institutions, funding agencies, and data management organizations that aims to improve the flow of information in research management by developing standardized data dictionaries and interoperable data exchange protocols". Their GitHub organization https://github.com/casrai appears empty/abandoned. Initially, the corporate site looks nice https://casrai.org/ but on closer inspection someone is using it to plug their religion. I'm confused, I thought we were talking about ontologies for research. Or maybe, God really is everywhere, including websites?

### Zenodo

- https://zenodo.org/
- They store research products, and issue persistent identifiers.

### OpenRIF

- GitHub Organization: https://github.com/openrif
- Open Research Information Framework
- http://www.openrif.org/ (Dead)
- Not http://www.openrif.com/ (Unrelated)
- https://figshare.com/articles/presentation/OpenRIF_and_VIVO/3180373

### Force16 Attribution Work Group

- that exists, apparently

---

## Ontologies

- [CRediT](#CRediT)
- [Contribution Ontology](#Contribution-Ontology)
- [Contributor Role Ontology](#Contributor-Role-Ontology)
- [Zenodo metadata](#Zenodo-metadata)
- [SCoRO](#SCoRO)
- [Habermann](#Habermann)
- [sdruskat.net](#sdruskatnet)
- [schema.org / codemeta](#schemaorgcodemeta)
- [Allcontributors](#Allcontributors)

### CRediT

- Developed within the context of [CASRAI](#CASRAI)
- CRediT: Contributor Roles Taxonomy
- Been around since 2014
- Originates from healthcare research domain
- Focused more on data management and project management than software (but still has a `Software` role)
- Taxonomy aims to specify how to attribute credit to individual contributors to a research project (which may include research software)
- _Credit Where Credit Is Due_ Eos article https://eos.org/opinions/credit-where-credit-is-due
- Formalized in 2022 as an ANSI/ISO standard: https://www.niso.org/press-releases/contributor-roles-taxonomy-credit-formalized-ansiniso-standard
    - https://credit.niso.org/
- Used by AGU since 2017
- (Being) adopted by Cell Press, PLOS and many other publishers (https://credit.niso.org/adopters/), and has been integrated into some submission and peer review systems and research workflow tools.
- Defines 14 roles
    1. `Conceptualization`
    2. `Data Curation`
    3. `Formal Analysis`
    4. `Funding Acquisition`
    5. `Investigation`
    6. `Methodology`
    7. `Project Administration`
    8. `Resources`
    9. `Software`
    10. `Supervision`
    11. `Validation`
    12. `Visualization`
    13. `Writing – Original Draft` # beware! emdash why?
    14. `Writing – Review & Editing` # beware! emdash why?
- Extended by the [Contributor Role Ontology](#Contributor-Role-Ontology) (not to be confused with the [Contribution Ontology](#Contribution-Ontology) to be described next)
- Ontology does not define a catch-all `Other` term. This leads to ambiguity for contributors who do not have a role assigned: is their role unknown, is their role omitted by mistake, does their role not fit with any of the terms?

### Contribution Ontology

- Deprecated, redirect to [Contributor Role Ontology](#Contributor-Role-Ontology).
- https://github.com/openrif/contribution-ontology/blob/731b1e321ebeaf22ecf977e472c383fe510f10c3/src/cro.owl defines the following taxonomy:
    1. `Author Role`
        1. `Editing and Proofreading Role`
        1. `Figure Development Role`
        1. `Translator Role`
        1. `Writing Original Draft Role`
    1. `Background and Literature Search Role`
    1. `Communication Role`
        1. `Documentation Role`
        1. `Graphic Design Role`
        1. `Marketing Role`
        1. `Networking Facilitation Role`
        1. `Website Development Role`
    1. `Conceptualization Role`
    1. `Data Role`
        1. `Data Aggregation Role`
        1. `Data Analysis Role`
            1. `Statistical Data Analysis Role`
        1. `Data Collection Role`
        1. `Data Curation Role`
            1. `Metadata Application Role`
        1. `Data Entry Role`
        1. `Data Integration Role`
        1. `Data Modeling Role`
        1. `Data Quality Assurance Role`
        1. `Data Standards Developer Role`
        1. `Data Visualization Role`
    1. `Educational Role`
        1. `Educational Material Development Role`
        1. `Educational Program Development Role`
        1. `Teaching Role`
    1. `Funding Acquisition Role`
    1. `Information Technology Systems Role`
        1. `Hardware Systems Role`
        1. `Software Systems Role`
            1. `Database Administrator Role`
            1. `System Administrator Role`
    1. `Intellectual Property Advisor Role`
    1. `Methodology Role`
        1. `Guideline Development Role`
        1. `Protocol Creation Role`
        1. `Standard Operating Procedure Development Role`
        1. `Study Design Role`
        1. `Technique Development Role`
    1. `Policy Development Role`
    1. `Preservation Role`
        1. `Archivist Role`
        1. `Conservator Role`
        1. `Digital Preservation Role`
    1. `Project Management Role`
    1. `Regulatory Administration Role`
    1. `Research Instrumentation Role`
        1. `Device Development Role`
        1. `Equipment Technician Role`
        1. `Survey and Questionnaire Role`
    1. `Resource Provider Role`
    1. `Software Developer Role`
        1. `Code Review Role`
        1. `Computer Programming Role`
        1. `Software Architecture Role`
        1. `Software Design Role`
        1. `Software Engineering Role`
        1. `Software Project Management Role`
        1. `Software Testing Role`
        1. `Technical Writing Role`
    1. `Study Investigation Role`
    1. `Supervision Role`
    1. `Team Management Role`
    1. `Validation Role`

### Contributor Role Ontology

- GitHub repository: https://github.com/data2health/contributor-role-ontology/
- Extends CASRAI Contributor Roles Taxonomy (CRediT) https://casrai.org/credit/
- Replaces OpenRIF's Contribution Ontology https://github.com/openrif/contribution-ontology
- https://ontobee.org/ontology/catalog/CRO?iri=http://purl.obolibrary.org/obo/CRO_0000000 defines the following roles (some roles expand into more detailed descriptors):
    1. `acceptor role`
    1. `advisory role`
    1. `author role`
        - `technical documentation role`
        - `lay summary role`
        - `writing original draft role`
        - `writing review and editing role`
    1. `collection role`
        - `specimen collection role`
            - `primary collector role`
        - `acquisition role`
    1. `conceptualization role`
    1. `data role`
        - `data collection role`
        - `metadata role`
        - `data entry role`
        - `data integration role`
        - `data modeling role`
        - `data quality assurance role`
        - `data transformation role`
        - `data validation role`
        - `database role`
            - `database administrator role`
        - `data curation role`
    1. `discovery role`
    1. `education and training role`
        - `training material role`
        - `training program development role`
        - `instruction role`
    1. `formal analysis role`
        - `statistical analysis role`
    1. `funding acquisition role`
    1. `funding source role`
    1. `hardware role`
    1. `infrastructure role`
        - `intellectual property role`
        - `regulatory and compliance role`
        - `team management role`
        - `project management role`
        - `project, policy or program evaluation role`
        - `coordination role`
        - `evaluator role`
            - `survey and questionnaire development role`
    1. `instrumentation role`
        - `device development role`
        - `equipment technician role`
    1. `investigation role`
        - `technician role`
        - `community research partner`
    1. `librarian role`
        - `background and literature search role`
    1. `marketing and communication role`
        - `website role`
        - `documentation role`
            - `technical writing role`
        - `community engagement role`
        - `outreach materials development role`
    1. `methodology role`
        - `standards role`
        - `protocol creation role`
        - `study design role`
        - `technique development role`
    1. `modifier role`
    1. `patient advocate role`
    1. `peer review role`
        - `code review role`
        - `grant peer review role`
    1. `policy development role`
    1. `presenter role`
    1. `preservation role`
        - `curator role`
        - `archivist role`
        - `conservator role`
        - `digital preservation role`
        - `creator role`
    1. `project administration role`
    1. `resources role`
        - `translator role`
    1. `software role`
        - `software testing role`
        - `system administrator role`
        - `code review role`
        - `software architecture role`
        - `software design role`
        - `software engineering role`
        - `requirements analysis role`
    1. `standards development role`
    1. `submitter role`
    1. `supervision role`
    1. `validation role`
    1. `visualization role`
        - `figure development role`
        - `graphic design role`

### Zenodo metadata

https://github.com/zenodraft/metadata-schema-zenodo/blob/7a48a4d876e95589e6dfe833e27751dfc2120719/schema.json defines the following 21 roles:

1. `ContactPerson`
2. `DataCollector`
3. `DataCurator`
4. `DataManager`
5. `Distributor`
6. `Editor`
7. `HostingInstitution`
8. `Other`
9. `Producer`
10. `ProjectLeader`
11. `ProjectManager`
12. `ProjectMember`
13. `RegistrationAgency`
14. `RegistrationAuthority`
15. `RelatedPerson`
16. `Researcher`
17. `ResearchGroup`
18. `RightsHolder`
19. `Sponsor`
20. `Supervisor`
21. `WorkPackageLeader`

Seems to have similar scope as CRediT, data management, project management, funding. Doesn't have any term for software related contributions, forced to use `Other`!

### SCoRO

- SCoRO, the Scholarly Contributions and Roles Ontology
- Not very software centric
- https://sparontologies.github.io/scoro/current/scoro.html defines the following ontology


- `authorship contribution`
    - `approves final manuscript`
    - `prepares illustrations`
    - `prepares supplementary information`
    - `publishes data`
    - `revises manuscript`
    - `writes manuscript draft`
- `experimental contribution`
    - `builds and/or maintains instruments`
    - `collects data`
    - `creates novel organisms or cells`
    - `creates novel reagents`
    - `creates software`
    - `develops methodology`
    - `maintains IT infrastructure`
    - `maintains organisms or cell cultures`
    - `maintains research facility`
    - `obtains and/or prepared specimens`
    - `performs experiments`
    - `processes data`
    - `provided service`
    - `provides existing data`
    - `provides patients`
    - `provides reagents, specimens or materials`
    - `provides software`
    - `provides technical support`
    - `provides tools, equipment or facilities`
- `intellectual contribution`
    - `analyses data`
    - `conceives project`
    - `designs experiments`
    - `formulates research questions`
    - `interprets results`
    - `leads investigation`
    - `provides advice`
    - `undertakes modelling`
- `organizational contribution`
    - `Supervises, mentors or trains colleagues`
    - `controls project finances`
    - `ensures regulatory compliance`
    - `manages project`
    - `provides administrative support`
    - `secures funding`


### Habermann

Ted Habermann summarized the relations between 5 prexisting credit ontologies in a preliminary crosswalk (https://zenodo.org/record/4767798). The first column of that crosswalk is his label of a given concept in each ontology, but that implicitly creates a 6th ontology which I refer to here as the Habermann ontology.

1. `archivist`
1. `author`
1. `background and literature research`
1. `co-author`
1. `code review`
1. `collection`
1. `communication`
1. `community engagement`
1. `computer programming`
1. `conservator`
1. `contact person`
1. `contributor`
1. `contributorship`
1. `coordination`
1. `curator`
1. `data`
1. `Data Acquisition`
1. `data aggregation`
1. `data collection`
1. `data entry`
1. `data modeling`
1. `Data Processing Disclosure Control`
1. `data quality assurance`
1. `data standards developer`
1. `data transformation`
1. `data validation`
1. `database administrator`
1. `device development`
1. `digital preservation`
1. `documentation`
1. `editor`
1. `educational`
1. `educational instruction`
1. `educational material development`
1. `educational program development`
1. `educational training`
1. `equipment technician`
1. `evaluation`
1. `figure development`
1. `Funding or Sponsorship Acquisition`
1. `Funding provision`
1. `graphic design`
1. `guideline development`
1. `hardware systems`
1. `hosting institution`
1. `information technology systems`
1. `infrastructure`
1. `instrumentation`
1. `intellectual property`
1. `IT hardware systems design and implementation`
1. `lay synthesis of research output`
1. `marketing`
1. `metadata application`
1. `networking facilitation`
1. `original draft preparation`
1. `outreach materials development`
1. `owner`
1. `participant recruitment`
1. `policy development`
1. `preservation`
1. `principal investigator`
1. `producer`
1. `program administrator`
1. `project management`
1. `project member`
1. `protocol creation`
1. `publisher`
1. `registration agency`
1. `registration authority`
1. `regulatory administration`
1. `related person`
1. `relationship`
1. `requirements analysis`
1. `research conceptualization`
1. `resources`
1. `rights holder`
1. `Rights Management`
1. `software architecture`
1. `software design`
1. `software documentation`
1. `software engineering`
1. `software systems`
1. `software testing`
1. `sponsor`
1. `standard operating procedure development`
1. `standards development`
1. `statistical analysis`
1. `study design`
1. `supervisory`
1. `survey and questionnaire`
1. `system administrator`
1. `systems administration`
1. `team management`
1. `technical writing`
1. `technician`
1. `technique development`
1. `translator`
1. `user`
1. `validation`
1. `website development`
1. `website maintenance`
1. `work package leader`

### sdruskat.net

Preliminary roles taxonomy from Stephan's blog https://sdruskat.net/software-authorship/. Corresponding GitHub Repository: https://github.com/sdruskat/software-authorship

1. `Supervision`
1. `Resources`
1. `Funding`
1. `Outreach`
1. `Development`
1. `Data curation`
1. `Testing`
1. `Documentation`
1. `Conceptualisation`

### schema.org / codemeta

Probably fixable with Role "decorator" irrespective of what CFF ends up using: https://github.com/citation-file-format/cffconvert/issues/366

Note that Codemeta implicitly defines a list of `roleName` to be used within the `Role` context:

1. `Design`
1. `Architecture`
1. `Debugging`
1. `Maintenance`
1. `Coding`
1. `Documentation`
1. `Testing`
1. `Support`
1. `Management`

### Allcontributors

- Big pro: this is based on actual experience using it in many projects
- Open question: do these keys sufficiently cover contributions as they are valued in academia?

1. `audio`
1. `a11y`
1. `bug`
1. `blog`
1. `business`
1. `code`
1. `content`
1. `data`
1. `doc`
1. `design`
1. `example`
1. `eventOrganizing`
1. `financial`
1. `fundingFinding`
1. `ideas`
1. `infra`
1. `maintenance`
1. `mentoring`
1. `platform`
1. `plugin`
1. `projectManagement`
1. `promotion`
1. `question`
1. `research`
1. `review`
1. `security`
1. `tool`
1. `translation`
1. `test`
1. `tutorial`
1. `talk`
1. `userTesting`
1. `video`

## JATS

- JATS = Journal Article Tag Suite
- PDF specification: https://groups.niso.org/higherlogic/ws/public/download/21030/ANSI-NISO-Z39.96-2019.pdf, https://dx.doi.org/10.3789/ansi.niso.z39.96-2019 (652 pp because why not)
- Wikipedia https://en.wikipedia.org/wiki/Journal_Article_Tag_Suite
- Home page https://jats.nlm.nih.gov/
- Widely adopted standard for separating content and metadata of articles (mostly journal articles) from presentation;
- JATS aims to describe any of the following types of documents (although technically you can use other terms?):
    1. `abstract`
    1. `addendum`
    1. `announcement`
    1. `article-commentary`
    1. `book-review`
    1. `books-received`
    1. `brief-report`
    1. `calendar`
    1. `case-report`
    1. `clinical-instruction`
    1. `collection`
    1. `correction`
    1. `discussion`
    1. `dissertation`
    1. `editorial`
    1. `in-brief`
    1. `introduction`
    1. `letter`
    1. `meeting-report`
    1. `news`
    1. `obituary`
    1. `oration`
    1. `partial-retraction`
    1. `rapid-communication`
    1. `reply`
    1. `reprint`
    1. `research-article`
    1. `retraction`
    1. `review-article`
- JATS uses contributor roles from CRediT
- Contributor roles are only a small part of JATS. Haven't seen many places where users bring their own JATS formatted file which then makes their lives easier, mostly it's the other way around, users fill in a plethora of data which is then stored as JATS, with an option to export that data as JATS.
- Further reading
    - 2018 blog post on xml.com https://www.xml.com/articles/2018/10/12/introduction-jats/
    - Many publishers already use (output / input) JATS (e.g. AGU, https://www.loc.gov)
    - Journal indexing services that currently require JATS/XML formats
        1. Scopus
        2. Web of Science
        3. PubMed
        4. DOAJ (Directory of Open Access Journals)
        5. Crossref
    - Existing publishing systems have support for it (e.g. Janeway)
    - Current version of JATS is 1.3
    - Taylor and Francis publisher's Guide for JATS https://jats.taylorandfrancis.com/jats-guide/. Taylor and Francis is allegedly one of the world's leading academic publishers.
    - Taylor and Francis template for a JATS `Article` which for the case of describing software could be of `article-type` `Other` https://jats.taylorandfrancis.com/jats-guide/tools/download/article.xml. Types are defined under Topics: https://jats.taylorandfrancis.com/jats-guide/topics/article-type/

## JATS4R

- https://github.com/JATS4R
- JATS4R ([JATS](#JATS) for Reuse) is a working group devoted to optimising the reusability of scholarly content by developing best-practice recommendations for tagging content in JATS XML
- Online validator with meh UX: copy-paste from https://github.com/JATS4R/JATS4R-Participant-Hub/tree/19fcf35f519647e9cb0ca90215e5583a93a78191/examples, put it in a local XML file, then click the mini button "Browse" https://validator.jats4r.org/ to select it.

## JAMS

- https://github.com/jam-schema/jams
- Julien Colomb et al.
- project doesnt't seem stable/mature yet, needs testing in the real world with real users / cases / tooling
- https://github.com/jam-schema/jams/blob/fdc90f388378e24deba43928647c46ce5bca86f6/Jamschema_v1.yml defines
    1. `Conceptualization`
    2. `Data curation`
    3. `Formal Analysis`
    4. `Funding acquisition`
    5. `Investigation: data collection`
    6. `Methodology`
    7. `Project administration`
    8. `Resources`
    9. `Software`
    10. `Supervision`
    11. `Validation`
    12. `Visualization`
    13. `Writing – original draft` # note: emdash why
    14. `Writing – review & editing` # note: emdash why

    These terms are (conceptually) the same as the CRediT terms.

## Two possible setups

|     | Allcontributors concept                                       | CFF == Allcontributors | CFF == sdruskat.net + `Other` + `Artwork`    |
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
| 13. | Financial Support: for who provide financial support          |  `financial`           | `funding`                                    |
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

1. I introduced 2 new categories in the sdruskat column:
    1. `artwork`, this could be the target for `audio`, `video` and `design`
    2. `other`, to differentiate from the omission case.
1. mapping `Allcontributors:design` to `sdruskat.net:conceptualization` would feel like a mismatch; even though a designer conceptualizes something, the (visual) design is not what defines the software project
1. I crossed out podcasts as part of Allcontributors's definition of `audio`, IMO podcasts are `promotion`
1. All categories from sdruskat.net are actually used as targets in the mapping
1. Concepts such as "design", "architecture", and "conceptualization" are some of the most valued/prestigious categories for researchers, but they are not well represented in Allcontributors terms
1. One could use the `allcontributors` bot to do its thing; `CONTRIBUTORS.md` would then be the single source of truth about contributors. Then, use a to-be-created tool to sync `CONTRIBUTORS.md` to `CITATION.cff`, maybe based on GitHub aliases? Insert `contributors[i].alias` in CFF using `CONTRIBUTORS.md` when alias is missing from CFF; Don't add names (unsolvable problem)

### Conversion

- Apalike: N/A
- Bibtex: N/A
- Codemeta 3.0: `Role` and `roleName` allow you to write down the exact role name without the need for conversion, but consumption by machines is limited unless people choose to observe the implicit rule about `roleName` being an enum.
- Endnote: N/A
- Schema.org: `Role` and `roleName` allow you to write down the exact role name without the need for conversion, but consumption by machines is limited.
- RIS: N/A
- Zenodo, CRediT: see below

|     | from Allcontributors                        | to Zenodo                                          | to CRediT          |
| --- | ---                                         | ---                                                | ---                |
| 1.  | `audio`                                     |                                                    |                    |
| 2.  | `a11y`                                      |                                                    |                    |
| 3.  | `bug`                                       |                                                    |                    |
| 4.  | `blog`                                      |                                                    |                    |
| 5.  | `business`                                  |                                                    |                    |
| 6.  | `code`                                      |                                                    |                    |
| 7.  | `content`                                   |                                                    |                    |
| 8.  | `data`                                      |                                                    |                    |
| 9.  | `doc`                                       |                                                    |                    |
| 10. | `design`                                    |                                                    |                    |
| 11. | `example`                                   |                                                    |                    |
| 12. | `eventOrganizing`                           |                                                    |                    |
| 13. | `financial`                                 |                                                    |                    |
| 14. | `fundingFinding`                            |                                                    |                    |
| 15. | `ideas`                                     |                                                    |                    |
| 16. | `infra`                                     |                                                    |                    |
| 17. | `maintenance`                               |                                                    |                    |
| 18. | `mentoring`                                 |                                                    |                    |
| 19. | `platform`                                  |                                                    |                    |
| 20. | `plugin`                                    |                                                    |                    |
| 21. | `projectManagement`                         |                                                    |                    |
| 22. | `promotion`                                 |                                                    |                    |
| 23. | `question`                                  |                                                    |                    |
| 24. | `research`                                  |                                                    |                    |
| 25. | `review`                                    |                                                    |                    |
| 26. | `security`                                  |                                                    |                    |
| 27. | `tool`                                      |                                                    |                    |
| 28. | `translation`                               |                                                    |                    |
| 29. | `test`                                      |                                                    |                    |
| 30. | `tutorial`                                  |                                                    |                    |
| 31. | `talk`                                      |                                                    |                    |
| 32. | `userTesting`                               |                                                    |                    |
| 33. | `video`                                     |                                                    |                    |
|     | `-----------------`                         | `------------------`                               | `------------`     |
|     | **from sdruskat.net** + `Other` + `Artwork` | **to Zenodo**                                      | **to CRediT**      |
| 1.  | `conceptualization`                         | <`Other`                                           |                    |
| 2.  | `data`                                      | >`DataManager` >`DataCollector` >`DataCurator`     |                    |
| 3.  | `development`                               | <`Other`                                           |                    |
| 4.  | `documentation`                             | <`Other`                                           |                    |
| 5.  | `funding`                                   | >`Sponsor`                                         |                    |
| 6.  | `infrastructure`                            | >`HostingInstitution`                              |                    |
| 7.  | `other`                                     | ==`Other`                                          |                    |
| 8.  | `outreach`                                  | <`Other`                                           |                    |
| 9.  | `supervision`                               | >`Supervisor`                                      |                    |
| 10. | `testing`                                   | <`Other`                                           |                    |

Notes:

1. Zenodo schema terms can be safely ignored, whatever we come up with will most likely map to Zenodo's `Other` term regardless.


### Preliminary `roles` schema

This section describes how to update CFF's JSONSchema file for version 1.3.0. I wrote it for the enum from sdruskat.net + `other` + `artwork`, but it would conceptually be the same for any given enum.

Additionally, some folks have advocated for having a free text field as CFF contributor role. This would not be useful for downstream usage, consumption by machines, and could hamper automatic validation of the contributor roles. But maybe if we do it like I wrote in the schema below, you can have an element from an enum, or a dict key with an explanation:

```json
{
    "$schema": "http://json-schema.org/draft-07/schema",
    "additionalProperties": false,
    "definitions": {
        "role": {
            "type": "string",
            "enum": [
                "artwork",
                "conceptualization",
                "data",
                "development",
                "documentation",
                "funding",
                "outreach",
                "infrastructure",
                "other",
                "supervision",
                "testing"
            ]
        },
        "role-description": {
            "type": "string",
            "minLength": 1,
            "maxLength": 255
        }
    },
    "properties": {
        "roles": {
            "oneOf": [
                {
                    "$ref": "#/definitions/role"
                },
                {
                    "type": "array",
                    "uniqueItems": true,
                    "minItems": 1,
                    "items": {
                        "oneOf": [
                            { "$ref": "#/definitions/role" },
                            {
                                "type": "object",
                                "additionalProperties": false,
                                "minProperties": 1,
                                "properties": {
                                    "artwork": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "",
                                        "examples": [
                                            "audio artwork such as background music or sound effects",
                                            "video artwork such as cutscenes",
                                            "graphical design such as logo, iconography, visual design",
                                            "animations"
                                        ]
                                    },
                                    "conceptualization": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Formulation of the idea and goals of the software, design of main features and functionalities",
                                        "examples": [
                                            "principal investigator",
                                            "architect",
                                            "requirements gathering"
                                        ]
                                    },
                                    "data": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Integration of data in the software and ensures metadata is annotated and available",
                                        "examples": [
                                            "data provider",
                                            "statician",
                                            "data manager",
                                            "data curator"
                                        ]
                                    },
                                    "development": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Creation and maintenance of the software, making the software ready for release",
                                        "examples": [
                                            "programmer",
                                            "maintainer",
                                            "UI/UX designer",
                                            "release manager"
                                        ]
                                    },
                                    "documentation": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Writing of any documentation related to the software, including but not limited to writing of user guidelines, API documentation, technical reports, etc.",
                                        "examples": [
                                            "technical writer",
                                            "metadata curator"
                                        ]
                                    },
                                    "funding": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Acquisition or management of funding for effort and events that sustain the software",
                                        "examples": [
                                            "principal investigator",
                                            "work package leader"
                                        ]
                                    },
                                    "infrastructure": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Provision and maintenance of resources used and exposed by the software project, like computational infrastructure and cloud systems",
                                        "examples": [
                                            "system administrator",
                                            "cloud manager"
                                        ]
                                    },
                                    "other": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Any other role",
                                        "examples": []
                                    },
                                    "outreach": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Communication with end-users and stakeholders",
                                        "examples": [
                                            "training",
                                            "community manager",
                                            "user support"
                                        ]
                                    },
                                    "supervision": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Coordinating the project effort, possibly across organizational boundaries",
                                        "examples": [
                                            "coordinator",
                                            "project manager",
                                            "advisor",
                                            "team leader"
                                        ]
                                    },
                                    "testing": {
                                        "$ref": "#/definitions/role-description",
                                        "description": "Unit test, usability, integration tests, release test",
                                        "examples": [
                                            "reviewer",
                                            "reporting user"
                                        ]
                                    }
                                },
                                "required": []
                            }
                        ]
                    }
                }
            ]
        }
    },
    "required": [],
    "type": "object"
}
```

This would allow for YAML like this:

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
- conceptualization  # "conceptualization" is a string
```

```yaml
# contributor with multiple roles, as array,
# where free text can be added to explain
roles:
- supervision
- conceptualization: description of conceptualization
    # "conceptualization" is a key in a dict
    # should "conceptualization:" be valid (i.e. when its value is empty string)?
```

```yaml
# contributor with a role that doesn't fit the existing role names
# according to the metadata author
roles:
- other: description of the other activity
```

What's maybe a bit odd is that these 2 examples are the same:

```yaml
roles:
  - conceptualization
  - supervision: managing the little ones
  - artwork: doodling
```
```yaml
roles:
  - conceptualization
  - supervision: managing the little ones
    artwork: doodling  # seemingly wrong to omit the dash
```

The advantage of including an optional description is we can see if people need more roles / how they interpret existing role names.

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
1. All-contributors taxonomy: https://allcontributors.org/docs/en/emoji-key
1. Look into defining a dict with one key for each term to avoid confusion about array of roles
