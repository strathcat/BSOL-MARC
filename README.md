# BSOL MARC files

This is a rough & ready workflow for converting advanced search results from British Standards Online into MARC records for import to your LMS, using [MarcEdit](https://marcedit.reeset.net/).

This will work for institutions with subscription access to BSOL, but is not designed for use with the newer BSI Knowledge platform.

1. Carry out an [Advanced Search](https://bsol.bsigroup.com/AdvancedSearch) for 'results in my subscription' where Update type = 'All' and set the 'From' and 'To' dates as required.[^1]
2. Click the 'Export Results' button to get a CSV file with your results. MarcEdit's *Delimited Text Translator* tool should be able to deal with any delimited format, but if you have problems with this file try re-saving it in Microsoft Excel .xlsx format.
3. Open the *Delimited Text Translator* in MarcEdit. Select the CSV file as the source and click 'Import'.
4. On the next screen click 'Load' and select **BSOL DTT template.mrd**. Select 'Ignore Header Row' and click 'Finish'.
5. Open the new .mrk file in MarcEdit and run the edit task **BSOL title list transformation.task**
6. Make any other changes you need to the records and save in .mrc format.

[^1]: If you want to export records for **all** your BSOL entitlements you will probably need to filter the results by module and export in several batches. BSOL does not permit exports of more than 4,000 results at a time.