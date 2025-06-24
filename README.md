# Science test cases SRCNet v0.1

## Description

This repository supports the development and coordination of **science test cases** for the SRCNet v0.1 test campaigns in the context of **Science Delivery** and is part of the [SP-5206 feature](https://jira.skatelescope.org/browse/SP-5206) in PI26 and [SP-5593](https://jira.skatelescope.org/browse/SP-5593) in PI27 (restricted access to collaborators).

The text below outlines the content and usage of the notebooks included in this repository. Detailed documentation about the Science Delivery contribution to SRCNet v0.1 Test Campaigns can be found on this [splash page on SKAO confluence](https://confluence.skatelescope.org/x/nCAAEw) (restricted access to collaborators). 

### Purpose

- Defining user "science test cases" that will exercise real v0.1 functionality.
- Documenting hardware and software environment requirements for running science test cases, to assist operations.
- Designing and implementing computational science test cases.

### Component details

The repository provides the notebooks and requirements necessary to run the v0.1 science test cases. These 11 tests (including 4 visualisation tests that are not included in the repository) will be carried out on 9 v0.1 SRC nodes. They are the following (also listed on this [summary page](https://confluence.skatelescope.org/display/SRCSC/v0.1+Test+campaign+-+Test+descriptions)):
* SWF-001 - Visualize Imaging Data Products with 4 subtests ([T1](https://confluence.skatelescope.org/x/g8ESEw), [T2](https://confluence.skatelescope.org/x/jsESEw), [T3](https://confluence.skatelescope.org/x/lsESEw), [T4](https://confluence.skatelescope.org/x/m8ESEw))
* SWF-002 - Catalogue Search and Crossmatch ([T1](https://confluence.skatelescope.org/x/0JUSEw))
* SWF-003 - Smoothing and Resampling ([T1](https://confluence.skatelescope.org/pages/viewpage.action?pageId=319987925))
* SWF-005 - Retrieve and import archival data including postage stamps ([T1](https://confluence.skatelescope.org/x/AqkSEw))
* SWF-006 - Change sky projection ([T1](https://confluence.skatelescope.org/x/B6kSEw))
* SWF-008 - EoR power spectrum estimation (with two subtests, [T1](https://confluence.skatelescope.org/pages/viewpage.action?pageId=319987896) and [T2](https://confluence.skatelescope.org/x/o2FoEw))
* SWF-010 - Continuum source finding ([T1](https://confluence.skatelescope.org/x/5pUSEw))
All the tests in the repository are based on Python; visualisation tests use CARTA.

Before executing any of these tests, the operator should follow the instructions (detailed on [this page](https://confluence.skatelescope.org/display/SRCSC/v0.1+Test+campaign+-+Testing+instructions) and summarised below)
1. Log in to the Gateway
2. Discover the data
3. Stage the data to the relevant node
4. Access CANFAR through the Gateway
5. Create a new CANFAR session
** Using CARTA
** Using Jupyter notebooks
6. Run the notebook tests
7. Run the CARTA tests
8. Validate the results and fill in the report
For each node/test performed, the reporting must be done according to [this template](https://confluence.skatelescope.org/display/SRCSC/Test+campaign+v0.1+reporting%3A+template) in a dedicated Confluence page (the link to each node-specific reporting page is given [here](https://confluence.skatelescope.org/pages/viewpage.action?pageId=318775452). The simplified reporting instructions are the following:
1. Associate Jira tickets
2. Confirm the general checks 
3. Run each test and report the outcomes by:
   ** Indicating the success level on the test-specific checks
   ** Fill out the detailed reporting for each test if necessary to report any error

### Inputs and outputs

All of the tests require datasets. The necessary datasets have been already imported into the datalake using Rucio and should be discoverable following the [testing instructions](https://confluence.skatelescope.org/display/SRCSC/v0.1+Test+campaign+-+Testing+instructions). If not, please report it in your node-specific reporting page.

### Use case

For an overview, check the demo presented at [2025-05-22 Demos & Discussion](https://confluence.skatelescope.org/x/eXjGEg) (Western) with the title "Science Delivery contribution to SRCNet v0.1 Test Campaigns".

For each test, follow the [testing instructions](https://confluence.skatelescope.org/display/SRCSC/v0.1+Test+campaign+-+Testing+instructions).

### Software requirements

Software requirements are detailed in the `requirements.txt` file, as well as in a dedicated requirements file in the test's sub-directory when necessary.

All the tests in the repository are based on Python; visualisation tests use CARTA.

### Hardware requirements

There are no specific hardware requirements.

### Directory Structure description of the repository

The repository is composed of a few sub-directories and files which serve different purpose.

Common files (main repository):
- README.md is the README file you are currently reading.
- LICENSE describes the license of the directory, i.e. BSD 3-Clause License.
- `requirements.txt` describes the python packages required to run the tests sucessfully.
- `config/` is a place holder for the path to the test datasets.

For each test case with ID, there is a repository
- `testcase_ID/` corresponding to an individual science test cases and a science workflow.
- `testcase_ID/tescase_ID.ipynb` is the notebook required to run the test.
Some repositories have an additional text file describing the python requirements to run this specific test.

## Contributors

This work is led by the Teal team in collaboration with other Agile teams, and the Project Scientists, especially for defining test cases that reflect realistic scientific use.

