1. Creating a Pluggable Database (PDB)
To create a pluggable database
 This example assumes a user-defined tablespace (plsql_class2024db), admin user (ke_plsqlauca)


```sql
-- Create a Pluggable Database (PDB)
CREATE PLUGGABLE DATABASE plsql_class2024db
ADMIN USER ke_plsqlauca IDENTIFIED BY MyPassword
ROLES = (DBA)
DEFAULT TABLESPACE users
FILE_NAME_CONVERT = (C:\app\HP\product\21c\oradata\XE\XEPDB1', '/opt/oracle/oradata/my_pdb/');

```