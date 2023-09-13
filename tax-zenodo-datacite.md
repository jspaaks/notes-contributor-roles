# Zenodo / DataCite metadata

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

Zenodo uses DataCite taxonomy for their contributor roles. https://schema.datacite.org/meta/kernel-4.3/doc/DataCite-MetadataKernel_v4.3.pdf