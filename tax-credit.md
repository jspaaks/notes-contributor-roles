# CRediT Taxonomy

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
- Extended by the [Contributor Role Ontology](tax-contributor-role-ontology.md) (not to be confused with the [Contribution Ontology](tax-contribution-ontology.md))
- Ontology does not define a catch-all `Other` term. This leads to ambiguity for contributors who do not have a role assigned: is their role unknown, is their role omitted by mistake, does their role not fit with any of the terms?
- There is talk of supporting CRediT in pkp-lib, https://github.com/pkp/pkp-lib, a library shared by Open Journal Systems (OJS), Open Conference Systems (OCS), Open Monograph Press (OMP), Open Preprint Systems (OPS) and Open Harvester Systems (OHS). https://github.com/pkp/pkp-lib/issues/857
- Tenzing: online form that generateas CRediT from a CSV Google Sheet: https://rollercoaster.shinyapps.io/tenzing/
- https://credit.niso.org/ defines 14 roles
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
