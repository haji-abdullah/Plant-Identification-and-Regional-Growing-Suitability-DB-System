# Plant Identification and Regional Growing Suitability Database System

**Database Systems Semester Project**

**Group:** G-15 Queries Crew

**Team Members:**

| Name          | Roll Number |
| ------------- | ----------- |
| Subhan Zahoor | BCSF25M003  |
| Haji Abdullah | BCSF25M004  |

**DBMS:** PostgreSQL

**Document:** Project Requirements Document (PRD)

**Status:** Phase 1 project document

---

## 1. Project Overview

Many people see a plant in a park, garden, nursery or public space but do not know its name. Even when they know a plant's name, they may not know whether it is suitable for the conditions in their area or how to care for it.

This project aims to provide an organized system for exploring plant information and finding possible plant matches through selected characteristics. A user will be able to choose characteristics such as flower colour, flower shape, leaf type and plant size. The system will compare those choices with the plant information available in the system and display possible matches, placing plants with more matching characteristics higher in the results.

Users will also be able to explore information about a plant, including its scientific and common names, taxonomic classification, growing requirements, care guidance, safety information, conservation information where reliable data is available, and regional suitability within selected areas of Pakistan.

The system is intended to support informed exploration and selection. **It does not identify plants with certainty.** It suggests possible matches based on the characteristics selected by the user. Results must be treated as suggestions rather than confirmed botanical identification.

The project will focus on selected regions of Pakistan. Regional suitability information will be provided where sufficient botanical and climatic information is available. The system will clearly distinguish unavailable information from information that indicates a plant is unsuitable.

The project will not use AI-based image recognition or identify plants from photographs.

## 2. Problems the Project Aims to Address

The system is intended to address the following problems:

1. People may see a plant but have difficulty finding its name when they do not know what to search for.
1. People may choose plants that are not well suited to their local growing conditions, reducing their chances of growing them successfully.
1. Plant information is spread across books, websites and other sources, making it difficult to explore related information in one place.
1. People may not be aware of recorded toxicity risks associated with some plants and their potential effects on children or pets.
1. Plant information may be presented without clear source references, making it difficult for users to judge where the information came from or whether it has been reviewed.
1. Users may struggle to compare plants by their visible characteristics, growing requirements and suitability for a particular region.

The system will help users explore these issues, but it will not guarantee that a selected plant will survive in a particular location. Actual growth can also depend on care practices and local conditions.

## 3. Project Objectives

The project aims to:

* Help users find possible plant matches by selecting visible characteristics.
* Bring available botanical, growing, care and safety information together in one place.
* Help users explore plants with recorded suitability information for selected regions of Pakistan.
* Make relevant safety warnings visible and distinguish unknown safety information from verified information.
* Maintain source references for submitted plant information.
* Provide a review process that distinguishes verified, pending and rejected submissions.
* Make missing or unavailable information visible instead of filling gaps with guesses.
* Provide useful summaries and reports about plants, regions, searches and verification activity.

## 4. Intended Users and Stakeholders

| User or stakeholder         | Intended activities                                                                                                                      |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Home gardener               | Search for possible plant matches, explore growing requirements and care guidance, and check available regional suitability information. |
| Nursery user or plant buyer | Explore plants by visible characteristics and growing conditions before selecting or recommending a plant.                               |
| General user                | Browse plant information, search for plants and view their own search history.                                                           |
| Contributor                 | Submit plant information with supporting source references for review.                                                                   |
| Verifier                    | Review submitted information against its supporting sources and approve or reject submissions with an explanation where appropriate.     |
| Administrator               | Manage user access, maintain system information and oversee verification activities and reports.                                         |

The exact permissions and administrative responsibilities will be refined during a later project phase. However, contributors will not be allowed to approve their own submissions, and ordinary users will not be allowed to alter stored search records.

## 5. System Features and Expected Behaviour

### 5.1 Search by Plant Characteristics

Users will be able to select characteristics from available lists. These may include:

* Flower colour
* Flower shape
* Leaf type or shape
* Plant size
* Other visible characteristics included in the system

Users may also select available growing preferences or requirements, such as sunlight needs or water requirements.

The system will compare the selected criteria with the available plant information and display possible matches in ranked order. Plants matching more of the selected criteria will generally appear before plants matching fewer criteria.

The system will:

* Show partial matches when no plant matches every selected criterion.
* Indicate how many selected criteria match each result.
* Clearly distinguish matching, non-matching and unavailable information.
* Avoid treating missing information automatically as either a match or a mismatch.
* Avoid presenting a partial match as a confirmed plant identification.

The exact search scoring and tie-breaking method will be finalized during a later phase.

### 5.2 Plant Information

When users open a plant record, the system may display the following information where it is available and supported by a reliable source:

* Scientific name and common names, including local names such as Urdu names.
* Taxonomic classification, including available levels such as Kingdom, Family, Genus and Species.
* Minimum and maximum height.
* Growing requirements, such as sunlight, water, soil type and pH range.
* Care guidance, such as watering, pruning and fertilizing, including available frequency or seasonal information.
* Recorded toxicity information for children or pets, including severity and reported symptoms where supported by reliable sources.
* Conservation information where reliable assessment data is available.
* Regions of Pakistan for which suitability information is available.
* Source references and the review status of submitted information.

Not every field will necessarily be available for every plant. The system will display unavailable or unknown information clearly and will not invent values to fill gaps.

### 5.3 Exploring Plants by Region

Users will be able to select from the regions of Pakistan covered by the system and explore plants with recorded suitability information for those regions.

Users may combine a region selection with additional criteria, for example:

* Plants recorded as suitable for a selected region that require relatively little water.
* Plants for a selected region that prefer full sunlight.
* Plants recorded as suitable for more than one selected region.

The system will only make regional suitability claims where supporting information is available. Unknown suitability will not be treated as proof that a plant is either suitable or unsuitable.

The project will initially cover selected regions rather than promise complete coverage of every area in Pakistan.

### 5.4 Browsing Plant Classification

Users will be able to explore available plant classification information. For example, they may open a plant family, view the genera recorded under it and explore the plants associated with those genera.

The system may also show counts, such as the number of recorded plants in a family or genus. These counts will describe the information available in the system, not the total number of plants that exist in nature.

### 5.5 Plant Safety Information

The system will display recorded toxicity warnings for children or pets when supported by reliable information.

It will distinguish between:

* Plants with recorded toxicity information.
* Plants for which reliable safety information is unavailable.
* Information that has not yet been reviewed or verified.

The absence of a recorded toxicity warning will not be presented as proof that a plant is safe. Users will be able to explore plants with recorded serious warnings, but the system will not provide medical or veterinary diagnosis or treatment advice.

### 5.6 Submitting and Reviewing Plant Information

Contributors will be able to submit plant information and provide supporting source references.

Expected behaviour:

1. Newly submitted information will be marked as pending review.
1. A verifier or authorized administrator will review the submission and its supporting source.
1. The reviewer may approve or reject the submission and may provide an explanatory note.
1. A contributor will not be allowed to approve their own submission.
1. Users will be able to distinguish verified, pending and rejected information.
1. Information that has not been reviewed will not be presented as verified.

Verification status must not be misleading. For example, if a plant's scientific name has been verified but its toxicity information has not, the system must not imply that all information about the plant is verified. The status of the relevant information must remain clear.

Where different sources provide conflicting information, the system will retain the relevant source references and will not silently present the conflict as settled or verified. Such information may require further review.

The precise scope of verification, including whether review applies to an entire plant record or to individual submitted information, will be finalized during a later phase.

### 5.7 Search History and Reports

The system will record searches and the criteria selected by users so that search activity can be reviewed.

Expected behaviour:

* Users will be able to view their own search history.
* Ordinary users will not be able to modify or delete stored search records.
* Administrators will be able to view aggregated reports for system analysis.

Possible reports include:

* Most frequently selected search characteristics.
* Plant submissions waiting for review.
* Plants with missing growing or care information.
* Contributors with the highest number of approved submissions.
* Sources associated with the highest number of approved submissions.
* Regions with the highest number of plants having recorded suitability information.
* Plant families and genera with the largest number of records.

Reports about sources will be based on source references associated with submitted information and its review status. Counts will describe the system's stored data, not necessarily all plants or all source material available outside the system.

## 6. Scenarios the System Should Handle

### Scenario 1: Finding a Possible Plant Match

A user sees a small plant with blue, star-shaped flowers in a park in Lahore. The user selects “blue flower”, “star-shaped flower” and “small” in the search.

The system displays plants with the greatest number of matching characteristics first. The user can compare the results and open a plant record to explore its available information.

The result is presented as a possible match, not a confirmed identification.

### Scenario 2: Exploring Plants for a Hot and Dry Region

A user living in a hot and dry area of Sindh wants to explore plants that may be suitable for the local conditions and require relatively little water.

The user selects the relevant region and the low-water requirement. The system displays plants for which supporting regional suitability and growing requirement information is available.

The system does not recommend a plant solely because its general description mentions a hot or dry climate. It uses the available plant requirements and regional evidence, and indicates when information is unknown.

### Scenario 3: Checking Recorded Safety Information

A parent wants to check whether a plant at home has recorded toxicity risks for children.

The user searches for the plant and views its available safety information, including severity and reported symptoms where supported by reliable sources.

If reliable toxicity information is unavailable, the system displays the status as unknown or unavailable. It does not imply that the plant is safe.

### Scenario 4: No Plant Matches Every Selected Characteristic

A user selects four characteristics, but no plant record matches all four.

The system still displays partial matches, placing plants with more matching available characteristics first. It indicates how many criteria matched and does not describe a partial match as a confirmed identification.

### Scenario 5: No Available Plant Matches the Search

A user selects characteristics for which no plant record has a match.

The system clearly informs the user that no matching plants were found in the available records. It does not invent results.

### Scenario 6: A Contributor Submits a Plant

A contributor submits information about a plant and provides supporting source references.

The submission is marked as pending review. If supporting information is missing or insufficient, the submission may remain pending or be rejected during review. It is not automatically treated as reliable.

### Scenario 7: A Verifier Approves Information

A verifier reviews a submission against its supporting source and approves it.

The approved information displays its verification status, the reviewer and the review date. Other information about the same plant that has not been verified remains clearly identified as unverified or pending.

### Scenario 8: A Contributor Attempts to Approve Their Own Submission

A contributor attempts to approve information they submitted.

The system does not allow the contributor to approve their own submission. The submission remains available for review by an authorized verifier or administrator.

### Scenario 9: A Verifier Rejects Incorrect Information

A verifier finds that submitted information does not agree with its supporting source.

The verifier rejects the submission and may provide an explanation. The rejected submission remains marked as rejected and is not presented as verified. Other independently verified information about the same plant may still be displayed with its own status.

### Scenario 10: A User Submits Invalid Information

A user attempts to submit information such as:

* A minimum height greater than the maximum height.
* A minimum pH value greater than the maximum pH value.
* A care frequency of zero days where a positive interval is required.
* A scientific name that already exists in the system.

The system informs the user that the submitted information is invalid and does not accept the invalid submission.

### Scenario 11: Information Is Missing

The system has a plant's name and taxonomic classification, but its water requirement is unknown.

The system still displays the available plant information and clearly marks the water requirement as unknown or unavailable. It does not guess a value.

The plant may appear in reports about incomplete information. It is not automatically treated as suitable or unsuitable for a low-water search criterion.

### Scenario 12: A User Attempts to Change Search History

A normal user opens their search history and attempts to edit or delete an old search.

The user can view their own search history but cannot modify or delete stored search records.

### Scenario 13: Exploring a Plant Family

A student opens a plant family and explores the genera and plants recorded under it.

The system displays the available classification hierarchy and the number of plant records in each group. These counts reflect the system's records only.

## 7. Project Scope: What Is Included

The project is intended to include:

* Searching for possible plant matches using selected characteristics.
* Ranking search results according to matching available criteria.
* Browsing plant names and available taxonomic classification.
* Viewing available growing requirements and care guidance.
* Exploring recorded regional suitability for selected areas of Pakistan.
* Viewing recorded toxicity warnings and their information status.
* Viewing conservation information where reliable data is available.
* Supporting multiple common and local names for a plant.
* Recording source references for submitted information.
* Allowing contributors to submit information for review.
* Allowing authorized verifiers or administrators to approve or reject submissions.
* Distinguishing verified, pending, rejected and unavailable information.
* Viewing personal search history and aggregated administrative reports.
* Validating submitted information and preventing invalid or inconsistent records.
* Providing different access permissions for different user roles.

The project will primarily be delivered as a PostgreSQL-based database system and demonstrated through the agreed project workflow. A separate website or mobile application is optional and will only be considered if time permits.

## 8. Project Scope: What Is Not Included

The following are outside the intended scope:

* Complete coverage of every plant or every region in Pakistan.
* Regional suitability guidance for countries outside Pakistan.
* Buying or selling plants, payments, orders or nursery stock management.
* Social features such as posts, comments, likes or chat.
* A full website or mobile application as a mandatory deliverable.
* Live weather observations or weather forecasts.
* Automatic plant identification from photographs.

## 9. What the System Will Not Do

The system will not:

* Identify a plant from an uploaded photograph.
* Guarantee that a suggested plant match is the correct identification.
* Guarantee that a plant will survive in a selected region.
* Treat missing botanical, growing or toxicity information as proof that a plant is suitable, unsuitable or safe.
* Invent missing information or silently replace unknown values with guesses.
* Provide medical or veterinary diagnosis or treatment advice.
* Replace advice from qualified botanical, medical or veterinary professionals.
* Detect plant diseases or pests.
* Provide live weather data or forecasts.
* Provide regional suitability guidance for countries outside Pakistan.
* Claim to cover every plant found in Pakistan.
* Allow contributors to approve their own submissions.
* Present pending or rejected information as verified.
* Send automated reminders for watering or other care tasks. Care schedules are provided for reference only.

## 10. Expected Final Outcome

By the end of the semester, the team intends to deliver a working plant information and regional suitability system that:

* Helps users find possible plant matches using selected visible characteristics.
* Provides botanical information, growing requirements, care guidance and safety warnings where reliable information is available.
* Helps users explore plants with recorded suitability information for selected regions of Pakistan.
* Allows contributors to submit plant information with supporting source references.
* Provides a review process through which submitted information can be approved or rejected by authorized users.
* Clearly distinguishes verified, pending, rejected and unavailable information.
* Provides useful reports about plants, regional suitability, search activity and verification progress.
* Handles incomplete or invalid information transparently without presenting guesses as facts.

The final demonstration will show how the system handles the user scenarios and requirements described in this document.

## 11. Questions the System Should Be Able to Answer

The system is intended to support questions such as:

1. Which plants best match selected characteristics such as blue flowers, small size and full sunlight?
1. Which plants have recorded suitability information for a selected region of Pakistan and require relatively little water?
1. Which plant families have the largest number of plant records?
1. Which genera have the largest number of recorded species?
1. Which plants have no care tasks recorded?
1. Which plants have recorded suitability information for more than one region?
1. Which plants have recorded serious toxicity warnings for pets, based on available verified information?
1. Which plants have recorded serious toxicity warnings for children, based on available verified information?
1. Which contributors have the highest number of approved submissions?
1. Which characteristics are selected most frequently in searches?
1. Which plant submissions are waiting for review?
1. Which plants have missing growing requirement information?
1. Which selected regions have the highest number of plants with recorded suitability information?
1. Which sources are associated with the highest number of approved plant information submissions?

The answers will reflect the information available in the system. They will not necessarily represent all plants, regions or source material outside the project.

## 12. Potential Data Sources

The team is evaluating the availability, reliability and permitted use of the following sources. These are potential sources, not a claim that every required data field is already available from them.

| Potential source                                          | Intended use                                                                                                                                                                                                 |
| --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Flora of Pakistan                                         | Botanical descriptions, taxonomy, plant families and information about distribution in Pakistan, where available.                                                                                            |
| GBIF                                                      | Taxonomic references and records of observed plant occurrences. Occurrence records will be treated as evidence of recorded observations, not automatic proof of cultivation suitability throughout a region. |
| Plants of the World Online (Kew)                          | Botanical taxonomy, accepted names and distribution information, where available.                                                                                                                            |
| Pakistan Meteorological Department                        | Regional climate information that may help describe the environmental conditions of selected areas. Climate information alone will not be treated as proof that a particular plant is suitable for a region. |
| Other reliable botanical, gardening and safety references | Additional information about growing requirements, care guidance and toxicity, where suitable sources can be identified.                                                                                     |

Different information categories may require different sources. For example, a taxonomy source may not provide detailed care schedules or toxicity information.

Before information is included, the team will evaluate source reliability, data availability and permitted use. Supporting source references will be retained for included information. Submitted information will be subject to the project's review process.

## 13. Assumptions and Limitations

The project is based on the following assumptions and limitations:

* Users can select or recognize basic visible characteristics such as colour, approximate size and leaf shape.
* The quality and coverage of search results depend on the accuracy and completeness of the plant information available in the system.
* Reliable botanical and regional information will be available for at least a selected set of plants and regions. The actual coverage will depend on the availability and quality of that information.
* Some plants will have incomplete information. The system will display these gaps rather than guess missing values.
* Regional suitability guidance will be limited to selected regions for which sufficient supporting information is available.
* Different sources may use different names, classifications or descriptions. These differences may require review before information is treated as verified.
* A plant's actual growth can depend on local conditions and care practices that are not fully represented in the system.
* The database and its required workflows are the main focus. A separate application is optional.

## 14. Decisions to Be Finalized in Later Phases

The following details remain open and will be finalized after further evaluation:

1. How Pakistan will be divided into regions, such as provinces, cities or climatic/agro-climatic zones.
1. Whether the initial plant collection will include only native plants or also introduced plants commonly grown in Pakistan.
1. The final list and categories of visible plant characteristics available for searching.
1. The exact search ranking, scoring and tie-breaking method.
1. The method used to distinguish unknown regional suitability from evidence of unsuitable conditions.
1. The conservation status reference or list to be used and its source.
1. Whether rejected submissions can be revised and submitted for review again.
1. The exact permissions of each user role.
1. Whether verification will apply to an entire plant record or to individual pieces of submitted information.
1. The minimum supporting evidence required before information can be approved.
1. How missing or conflicting information from different sources will be handled.
1. How regional suitability will be assessed using botanical requirements and regional climate information.
1. The exact information that ordinary users can see in their own search history and the reports available to administrators.

These decisions will be finalized during the relevant design and requirements phases. The team will not claim functionality or data coverage that has not been established.

---

**Document note:** This PRD describes the intended product, its users, expected behaviour, scenarios, scope and limitations. Detailed database entities, relationships, SQL commands, functions, triggers and implementation designs will be documented separately in the relevant project phases.
