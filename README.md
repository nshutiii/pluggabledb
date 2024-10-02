1. Creating a Pluggable Database (PDB)
To create a pluggable database
 This example assumes a user-defined tablespace (plsql_class2024db), admin user (ke_plsqlauca)



-- Create a Pluggable Database (PDB)
```sql
CREATE PLUGGABLE DATABASE plsql_class2024db
ADMIN USER ke_plsqlauca IDENTIFIED BY MyPassword
DEFAULT TABLESPACE users
FILE_NAME_CONVERT = (C:\app\HP\product\21c\oradata\XE\XEPDB1', 'C:\app\HP\product\21c\oradata\XE\XEPDB1\plsql_class2024db');

```

2. Deleting a Pluggable Database (PDB)
Before deleting a pluggable database, it must be closed and in MOUNT mode.


-- Close the PDB before dropping it
```sql
ALTER PLUGGABLE DATABASE my_pdb CLOSE IMMEDIATE;
```

-- Open the PDB in MOUNT mode
```sql
ALTER PLUGGABLE DATABASE my_pdb OPEN MOUNT;
```


-- Drop the Pluggable Database
```sql
DROP PLUGGABLE DATABASE my_pdb INCLUDING DATAFILES;

```
