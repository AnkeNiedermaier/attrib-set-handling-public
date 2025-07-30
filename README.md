# PythonPart AttribSetHandling
Since several Allplan versions it is possible to group attributes individually and assign them more or less automatically to selected objects in using so called **AttributsetTemplates** which are part of the project settings. With this PythonPart it is possible to edit such templates directly in Excel. It offers different options:
- **read** and **modify** already existing templates
- **add** aditional sets to already existing templates
- **create** completely new templates

This is possible both for single or a whole bunch of AttributSets.

## Installation
The PythonPart **AttribSetHandling** can be installed directly from the Plugin Manager in ALLPLAN. 

Alternatively, the corresponding ***.allep** package can be downloaded from the [release page](https://github.com/AnkeNiedermaier/attrib-set-handling-public/releases). ***.allep** files are ALLPLAN internal setups that can be installed via drag and drop into the program window.

At least the version 2026 is needed to install the PythonPart.

## Installed PythonPart Scripts
If the installation was successfull, the PythonPart **AttribSetHandling.pyp** can be found
in the ALLPLAN Library:
`Office` → `ALLPLAN GmbH` → `AttribSetHandling`

## Excel template
When reading off and exporting AttributsetTemplates it is possible to either **add them** to an already exising file or **create a new** independend one. It will be structured according to the requirements of the PythonPart.

Therefor NO predefined Excel template is installed with the PythonPart, as it can easily be created when running the export for the first time. Afterwards it can be copied and used for additional Attributsets.

Within the file, new sheets can be created, existing ones deleted and the content modified.

> ⚠️IMPORTANT\
The schema and structure of the Ecxel file is fixed and predefined and should not be changed, otherwise the PythonPart will not run correctly!

There is an individual sheet for each "assignment rule" which best should be named "**Attributset-Object; Attributset-Category**"

Both parameters also have to be entered within the first empty line in the columns with the same name. Already existing UID values can be kept, but there is no need to create them manually in new sets, as they will be added automatically during the runtime of the PythonPart.

In the following line the **name of the AttributGroup (CPSet)** in which the corresponding attributes are combined should be entered in the **CPSetName** column.