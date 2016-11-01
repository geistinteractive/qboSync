## 2.1.0

released 11/1/2016

  - enhancements:
    - add script comments to config scripts
    - add config option to include inactive QBO records in the sync
    - add option to not save a record downloaded from QBO
      - to accommodate this change, am now saving the qbo_id after saving other fields
      - also document a way to download Invoices without linking them to a Customer
    - move Validate BaseElements Plugin script to Public folder
	- add "button" script to validate plugin, and always show the status
  - bug fixes:
    - blank Invoice created when sync failed due to Inactive Customer not being downloaded
      - this bug may have shown up in other scenarios as well
    - Sync fails to Get more than the Batch Size


### 2.0.1

released 10/14/2016

  - bug fixes:
    - minor interface issues
    - normalize Accounts table occurrence naming
    - remove link to open an Item in QBO from iPad and iPhone layout (this feature no longer works)
	- add field validation to Item table, to match QBO's validation
	- re-organized fields on Item layouts
	- correct data in QBOEntity table
	- Item expense account isn't set
	- abort sync if the company changes