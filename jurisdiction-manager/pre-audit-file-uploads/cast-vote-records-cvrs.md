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
* The tabulator IDs will be parsed from the CVR using the first four digits of the Tabulator CVR field, including any leading zeros. The tabulator names in the manifest must be four digits and include any leading zeros in order to match.

**Hart:**&#x20;

* A Hart CVR export is a ZIP file containing an individual XML file for each ballot.
* Either a single ZIP file can be provided or multiple, one for each tabulator. When multiple ZIP files are provided, the ZIP file names (with ".zip" removed) will be used as tabulator names.
* Separate from the ZIP files, optional scanned ballot information CSVs can be provided. If provided, the "Workstation" values in them will be used as tabulator names, and the "UniqueIdentifier" values in them will be used as imprinted IDs. Otherwise, "CvrGuid" values will be used as imprinted IDs.
* If both multiple ZIP files are provided and scanned ballot information CSVs are provided, the ZIP file names will take precedence over the "Workstation" values as tabulator names.
* Note that tabulator names are only used if batch names in the ballot manifest are not unique.

The CVR export process may be tricky the first few attempts. We are happy to review files prior to upload and encourage all users to work through this process with us well before audit day. Many jurisdictions have used their logic and accuracy testing CVR files to practice.&#x20;

### Field Mapping by Voting System

<table><thead><tr><th width="171">Arlo</th><th width="150">ClearBallot</th><th width="150">Dominion</th><th width="150">ES&#x26;S</th><th>Hart</th></tr></thead><tbody><tr><td>CVR Unique ID</td><td>RowNumber</td><td>CvrNumber</td><td>Cast Vote Record</td><td>CvrGuid</td></tr><tr><td>Tabulator</td><td>ScanComputerName</td><td>TabulatorNum</td><td>Tabulator CVR (first four characters)</td><td>Each export must be for one tabulator</td></tr><tr><td>Batch</td><td>BoxID</td><td>BatchId</td><td>Batch</td><td>BatchNumber</td></tr><tr><td>Ballot Number</td><td>BoxPosition</td><td>RecordId</td><td>Inferred from row order in the file</td><td>BatchSequence</td></tr><tr><td>Imprinted ID</td><td>BallotID</td><td>ImprintedId</td><td>Tabulator CVR</td><td>CvrGuid</td></tr></tbody></table>

\
\
