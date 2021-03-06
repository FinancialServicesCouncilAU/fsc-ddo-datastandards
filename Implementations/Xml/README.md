# Xml

This folder defines the technical implementation of the FSC DDO Data Standards in an Xml Representation.   

It consists of three Data Standards:
- **[Target Market Determinations](/Canonical/TargetMarketDeterminations.md)**
    - [Target Market Determination Schema Documentation](https://financialservicescouncilau.github.io/fsc-ddo-datastandards/xml/TargetMarketDeterminations.html)
    - [Schema Definition](/Implementations/Xml/TargetMarketDeterminations.xsd)
- **[Complaints](/Canonical/Complaints.md)**
    - [Complaints Schema Documentation](https://financialservicescouncilau.github.io/fsc-ddo-datastandards/xml/Complaints.html)
    - [Complaints Schema Definition](/Implementations/Xml/Complaints.xsd)
- **[Dealings](/Canonical/Dealings.md)**
    - [Dealings Schema Documentation](https://financialservicescouncilau.github.io/fsc-ddo-datastandards/xml/Dealings.html)
    - [Dealings Schema Definition](/Implementations/Xml/Dealings.xsd)

There are also **Common Data Items**, shared by all Data Standards
    - [Common Schema Documentation](https://financialservicescouncilau.github.io/fsc-ddo-datastandards/xml/Common.html)
    - [Common Schema Definition](/Implementations/Xml/Common.xsd)

 ## Releasing a new version
  - Create a new target branch referencing to the new version
  - increment the version numbers in the schemas
  - Add the new version to the DataStandardVersionEnum in Common.xsd
  - complete version consistency checks (ie the version in all xsd should align to the branch)
  - regenerate all language implementations i.e. the C# code

## Data Standards
 - Suffix all enum types with *Enum
 - Suffix all Global Complex Types with *Type 
 - Suffix all arrays/lists with "*CollectionType"
 - All Collection Types should support a 0-unbounded min/max
 - Only have a single Global element that represents the root element of the report
 - Minimise use of anonymous types

 ***
 ## XSD Structure Overview
 ### Target Market Determinations Diagram
 ![TMDs Structure](Documentation/TargetMarketDeterminations.png)
 
 ### Dealings Diagram
 ![Dealings Structure](Documentation/Dealings.png)

 ### Complaints Diagram
 ![Complaints Structure](Documentation/Complaints.png)
 