# fmQBO2

user: admin
pass: [blank]

## Global Variables

| Name                            | Use
| ----------------------------    | ----
| $$QBOSync_id_Field              | name of field that holds the unique primary key value, as generted by FileMaker
| $$QBOSync_qbo_id_Field          | name of field that holds qbo id
| $$QBOSync_qbo_send_Field        | name of field that holds boolean value which determines if the record has changed since the last sync
| $$QBOSync_fmqbo_id_Field        | name of field in QBOSync table that is connected to Entity table's primary key field in the relationship graph
| CHILDREN
| $$QBOSync_child_id_Field        | realted record's primary key field (like InvoiceItem::id)
| $$QBOSync_child_id_parent_Field | related record's foreign key field, pointing to the current record (like InvoiceItem::id_Invoice)
| $$QBOSync_child_qbo_id_Field    | qbo id field of related record
| $$QBOSync_child_fmqbo_id_Field  | name of field in QBOSync that's connected to the child table
| OPTIONAL
| $$QBOSync_deleted_Field         | name of field that is set to 1 to delete the record during sync


## Development Conventions

Mostly just documenting stuff I think other developers working on this file should know.

1. $n is a 0-based javascript iterator and $i is a 1-based FileMaker iterator.
   * this concept was introduced as a refactor, so it's possible some old code doesn't follow this standard
2. A "Dispatch" script is one that calls a different script based on the current entity. My goal was to keep these as simple as possible. This is a config script for developers of fmQBO2.fmp12 (not for end-users, unless they're adding entities to sync, in which case I consider them a developer of fmQBO2.fmp12)
3. Various UI scripts determine which layout to go to based on the layout name, with a test like:  
   `RightWords ( Get ( LayoutName ) ; 1 ) = "iPad"`
4. Invoice layout uses an OnCommit Trigger to update the `qbo_send` value, which wont automatically be set to true when a users modifies an InvoiceItem record. It also summarizes InvoiceItems data and stores in the Invoice table. This same  process will have to be replicated in an end-users solution if they are using fmQBO2 for syncing only (and not for it's UI).


## Hidden Developer Tools

1. `Get From QBO and Copy Response` script, allows easy access to QBO's version of the record you are currently viewing in the UI. You have to find the script in Script Workspace to run it.
2. `QBOEntity` has a "Dev Tools" popover with a few options:
   1. Enable/Disable Logging  
      This is a _very_ simple system that stores QBO requests and responses in a repeating global variable. You are expected to view the log via the Data Viewer (or copy it for pasting into a text editor). This is really only designed for use by us, which is why I'm not mentioning it in the version history.
   2. Clear Log Data
   3. Delete ALL Synced Data  
      Useful for switching between test companies while developing; I've been having to switch between a company with shipping enabled and one with it disabled, this script has been useful for that.
