# qboSync

user: admin
pass: [blank]

## Global Variables

| Name                         | Use
| ---------------------------- | ----
| $$QBOSync_id_Field           | name of field that holds the unique primary key value, as generted by FileMaker
| $$QBOSync_qbo_id_Field       | name of field that holds qbo id
| $$QBOSync_qbo_send_Field     | name of field that holds boolean value which determines if the record has changed since the last sync
| $$QBOSync_deleted_Field      | name of field that is set to 1 to delete the record during sync
| $$QBOSync_fmqbo_id_Field     | name of field in QBOSync table that is connected to Entity table's primary key field in the relationship graph
