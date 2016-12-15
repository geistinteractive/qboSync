## 2.3.0

unreleased

  - enhancements:
    - allow syncing of shipping fields on an Invoice
  - bug fixes:
    - qbo_id in TaxCode is failing validation on GET
    - $$QBOSync_running in qbo_send auto-enter calculation does NOT work with external files
    - keeps getting same records from QBO
    - folder ending with .fmp12 causes Mac to display icon not folder
    - Deleting fails if the record is already gone
    - Don't create blank Invoice lines


## 2.2.0

released 11/8/2016

  - enhancements:
    - add an FM13 compatible interface file
    - improved window handling when Sync is started from an external file
      - will now show the sync progress and hide itself when done
    - add splashscreen style layout for when fmQBO2 is accessed from an external file
  - bug fixes:
    - deleted list items are displayed as their primary key from related records
    - value lists can't be accessed from external file


## 2.1.0

released 11/2/2016

  - enhancements:
    - add script comments to config scripts
    - add config option to include inactive QBO records in the sync
    - add option to not save a record downloaded from QBO
      - to accommodate this change, am now saving the qbo_id after saving other fields
      - also document a way to download Invoices without linking them to a Customer
    - move Validate BaseElements Plugin script to Public folder
    - add "button" script to validate plugin, and always show the status
    - add config option to prevent getting any data from QBO that was modified before a specified date
    - allow the last get timestamp to be changed, which can limit the data to get from QBO on a per-entity basis
  - bug fixes:
    - blank Invoice created when sync failed due to Inactive Customer not being downloaded
      - this bug may have shown up in other scenarios as well
    - Sync fails to Get more than the Batch Size
    - last get timestamp is always displayed in the timezone of the computer that did the sync (as opposed to the send timestamp which correctly showed the time in the current users timezone)
    - don't process children if parent's Get script generates an error


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