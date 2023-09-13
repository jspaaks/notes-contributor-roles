# JATS

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

