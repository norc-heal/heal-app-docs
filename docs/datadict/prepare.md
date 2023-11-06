# Special Considerations in Preparing Files for Ingest

Certain data files and data dictionaries may require additional steps or data files. See below for information on these specific circumstances.

## REDCap Data Dictionaries

## SAS Files

For tabular files saved in SAS (sas7bdat), you will want to have an accompanying catalog file (sas7bcat). Although the sas7bdat contains variabl metadata information (variable names and variable labels/descriptions), the sas7bcat contains information about the formats and encoding of the variables, which are important for producing a complete data dictionary.

### Creating a sas7bdat and sas7bcat file

{{ external_markdown('https://raw.githubusercontent.com/HEAL/healdata-utils/main/docs/vlmd/extract/sas.md', '## Creating a `sas7bdat` and a `sas7bcat` file') }}

### Running through the tool

After creating the necessary sas7bdat and sas7bcat files, you are ready to convert to a HEAL-compliant data dictionary using the data packaging tool. 

**First, ensure that your sas7bdat and sas7bcat files are saved in the same folder.** The tool will only ask you to select your sas7bdat file. If the sas7bcat file is located in the same directory, the tool will automatically detect it, as well. If not detected, the tool will run without the sas7bcat catalog file and the encodings (i.e., value labels) will not be extracted from the catalog file and will not appear in your data dictionary.