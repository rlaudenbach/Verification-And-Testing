# [Installation Verification And Testing] - Installation


## History

Release          | Notes                        | Supported Aras Versions
-----------------|------------------------------|-------------------
[v1](add link)   | Initial Release              | 12SP10, 12SP11, 12SP12, 12SP14

*add link to version location in repository on each row


## Important!
**Always back up your code tree and database before applying an import package or code tree patch!**


## Pre-requisites

1. Aras Innovator installed (supported version)
2. Aras Update Tool || Aras Package Import tool


## Installation

The installation can be done in oen of 2 ways:

1. Automated: Using the Aras Update tool (recommended) - Update version 1.9 or higher
2. Manually: Using the packages import tool 

### Automated: Using Aras Update

Log on as "admin"

1. start the Aras Update Tool
2. choose "local"
3. Click on "Add package reference"
4. On file dialog find installation folder "Installation" (where you extracted this solution package to locally) and click "OK"
5. Click on "install"
6. Review the install selection. Click on "Next"
7. Select "Detailed logging" and click on "Next"
8. Click on "Browse" and select your Aras installation folder (choose folder "Innovator")
9. Click on "Import into Innovator DB" and enter your connect parameters for "Innvator URL, Database, Innovator user (admin), User Password"
10. Click "Install" - wait until success message appears

NOTE: you must clear the browser cache of all clients after deploying the code tree patches.


### Manual Code Tree and Import Steps

#### Deploy Code Tree Changes
CodeTree patches are located in folder "...Installation\CodeTreePatches\Innovator" of this solution

1. Select folder "Innovator" and copy it
2. Navigate to the root folder of your Aras installation.  (i.e. "C:\Program Files (x86)\Aras_Innovator")
3. Paste the copied folder to the Aras installation root.
4. Confirm "Overwrite" warning.

NOTE: you must clear the browser cache of all clients after deploying the code tree patches.


#### Import Packages

The import of this solution requires 4 import cycles (3 are optional)

Import packages are located in folder "...Installation\imports" of this solution

Log on as "admin"

1. Open up the Aras Package Import tool.
2. Select relevant database and enter your login credentials for "root" and click **Login**

Cycle 1:
1. Enter the package name in the TargetRelease field.
2. Enter the path to your local *"...Installation\imports\1-imports.mf" file in the Manifest File field.
3. Select all packages in the Available for Import field.
4. Select Type = **Merge** and Mode = **Thorough Mode**.
5. Click **Import** in the top left corner.

Cycle 2 (optional):
1. Enter the package name in the TargetRelease field.
2. Enter the path to your local *"...Installation\imports\2-imports - PLM.mf" file in the Manifest File field.
3. Select all packages in the Available for Import field.
4. Select Type = **Merge** and Mode = **Thorough Mode**.
5. Click **Import** in the top left corner.

Cycle 3 (optional):
1. Enter the package name in the TargetRelease field.
2. Enter the path to your local *"...Installation\imports\3-imports - SA.mf" file in the Manifest File field.
3. Select all packages in the Available for Import field.
4. Select Type = **Merge** and Mode = **Thorough Mode**.
5. Click **Import** in the top left corner.

Cycle 3 (optional):
1. Enter the package name in the TargetRelease field.
2. Enter the path to your local *"...Installation\imports\4-imports - RE,SM.mf" file in the Manifest File field.
3. Select all packages in the Available for Import field.
4. Select Type = **Merge** and Mode = **Thorough Mode**.
5. Click **Import** in the top left corner.


## Installation Validation (quick steps)
1. log on as "admin" ....
2. Go to TOC main level.  Notice 1 new category "Verification and Testing"
3. Go to Administration/Identities and find new Identity "Verification and Testing".  Add users to its members (i.e. Mike Miller)
4. log on as "mmiller"
5. Go to "Verification and Testing/Test Plans" create a new Test Plan, Test Runs, etc. ....

... After this you have validated that the new functionality of this solution is available
Read the "Admin Guide" documentation to see how to make use of this new functionality.

## Contributing
For more information on contributing to this Presales Solution, send an email to the owner at "Technical Enablement"


## License
Aras Presales Solutions are published under the MIT license. See the [LICENSE.md file](./LICENSE.md) for license rights and limitations.
