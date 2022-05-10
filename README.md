# Field Museum of Natural History (FMNH) scripts
This repository contains miscellaneous scripts for use by FMNH staff, interns, and volunteers.  These scripts are generated within Google Colaboratory ("Colab").  The benefits of Colab include: in-browser Python code execution, instructions embedded within scripts, and usability by non-technologists.  To execute a Colab script, you must have and be logged into a Google account.

**To run any script:** click on the name (above) and then click the blue "Open in Colab" button that appears near the top of the page.  This will navigate you to the active script within Google Colab.

-----
#### Download_Image_Files_from_Pteridoportal.ipynb
- _About_: Download images from public-facing web databases for digitized herbarium collections, based on your search query.
- _Preconditions_: A stable internet connection, and local storage space for the files.
- _Inputs_: A data download from the [Pteridoportal](https://www.pteridoportal.org/portal/index.php) or other related portal site (e.g. [Bryophyte Portal](https://bryophyteportal.org/portal/)).
- _Outputs_: A ZIP file containing all of the image files.

-----

#### Microplant_Mystery_Zooniverse_Processing.ipynb
- _About_: Process a [Zooniverse]() classification results file by flattening JSON strings into columns, making it suitable for spreadsheet analysis.
- _Preconditions_: A Zooniverse account, an already-existing Zooniverse project which has gathered results (i.e. public participants).  Classification results file has been downloaded from Zooniverse.  Any rows that you don't wish to be processed (e.g. testing phase results) are deleted.
- _Inputs_: A CSV file, which has been uploaded to your Google Drive (in the root "My Drive" folder).
- _Outputs_: A ZIP file containing one CSV file for each Workflow.
- _Known Limitations_: Currently, only two types of Tasks are extracted:
  - Question
  - Drawing (rectangle tool)

-----

#### Test_train_split_an_image_set_with_metadata.ipynb
- _About_: Given a folder of images in Google Drive, this script creates a duplicate folder with train/test splits.
- _Preconditions_: A folder of images in Google Drive -- either a single folder with images and metadata intermingled, or multiple folders with only metadata in the root.  (For the latter, only can do stratified sampling).  Authenticate your Google Drive in Colab ([tutorial](https://colab.research.google.com/notebooks/io.ipynb#scrollTo=u22w3BFiOveA)).
- _Inputs_: A Google Drive folder containing one dataset.
- _Outputs_: A Google Drive folder (with editor access).
- _Known Limitations_:
  - Sampling is not random -- since our specimen image files are often named `specimen_id-image_count.tif` and are retrieved alphabetically, we sample images evenly across the entire folder.
  - In a flat folder

-----
### Acknowledgements

Thanks and credit to the Grainger Bioinformatics Center and FMNH botany collections.

Please consult the included license for information about use and redistribution.
