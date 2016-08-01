# qboSync

user: admin
pass: qbo

## Global Variables

| Name                         | Use
| ---------------------------- | ----
| $$QBOSync_id_Field           | name of field that holds the unique primary key value, as generted by FileMaker
| $$QBOSync_qbo_id_Field       | name of field that holds qbo id
| $$QBOSync_qbo_send_Field     | name of field that holds boolean value which determines if the record has changed since the last sync
| $$QBOSync_fmqbo_id_Field     | name of field in fmqbo table that is connected to Entity table's primary key field in the relationship graph
