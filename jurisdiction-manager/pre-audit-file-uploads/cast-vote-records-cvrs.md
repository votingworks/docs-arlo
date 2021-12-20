---
description: For ballot comparison and hybrid audits only.
---

# Cast Vote Records (CVRs)

### Cast Vote Record Requirements

When retrieving cast vote records (CVRs) from your voting system, it’s important to follow your system’s instructions to ensure proper export. Most systems export groups of CVRs in a single file, but some systems export each individual ballot’s record as a separate file.

The following data must be included for each ballot (names may vary by voting system - see chart below):&#x20;

* Unique ID for each CVR&#x20;
* Tabulator ID/name/number&#x20;
* Batch ID/name/number&#x20;
* Ballot position within a batch Imprinted ID (if applicable)&#x20;
* Recorded votes/marks for every contest on a particular ballot, each containing:
  * Contest name&#x20;
  * Candidate name&#x20;
  * Vote/mark (and override, if applicable)

**NOTE**: The “Tabulator name” and “Batch name” columns on your Ballot Manifest must match those found in the cast vote records.&#x20;

### Voting Equipment Specific Information&#x20;

As mentioned above, we strongly encourage you to follow the instructions provided by your vendor when retrieving the cast vote records from your voting system. Some tips we’ve learned from other jurisdictions are provided below.

**Dominion:**&#x20;

* The Cast Vote Record tabular box should be checked in the export menu
* Sometimes fields are exported with extra characters, like quotation marks and equal signs. To eliminate these extra characters, open the CVR file safely in Excel (open a blank worksheet, go to Data > From Text > select CVR file > Import) and use the ctrl-s function to re-save.

**ES\&S:**&#x20;

* ES\&S does not provide a single CVR export with all the data needed for the audit. Instead, two exports are required:&#x20;
  * Tools > Export Cast Vote Record&#x20;
  * Produce Module > Ballots - Table View > set filter to “all” > Export (this file only allows 20K records to be exported at one time and may require several exports depending on your number of ballots)&#x20;
* Overvotes must be listed as a contest selection and should not be selected as the voter voted&#x20;

**Hart:**&#x20;

* When multiple tabulators are used, CVRs must be exported by tabulator

The CVR export process may be tricky the first few attempts. We are happy to review files prior to upload and encourage all users to work through this process with us well before audit day. Many jurisdictions have used their logic and accuracy testing CVR files to practice.&#x20;

### Field Mapping by Voting System

| Arlo          | ClearBallot      | Dominion     | ES\&S                                 | Hart                                  |
| ------------- | ---------------- | ------------ | ------------------------------------- | ------------------------------------- |
| CVR Unique ID | RowNumber        | CvrNumber    | Cast Vote Record                      | CvrGuid                               |
| Tabulator     | ScanComputerName | TabulatorNum | Tabulator CVR (first four characters) | Each export must be for one tabulator |
| Batch         | BoxID            | BatchId      | Batch                                 | BatchNumber                           |
| Ballot Number | BoxPosition      | RecordId     | Inferred from row order in the file   | BatchSequence                         |
| Imprinted ID  | BallotID         | ImprintedId  | Tabulator CVR                         | CvrGuid                               |

\
\
