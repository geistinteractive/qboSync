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
