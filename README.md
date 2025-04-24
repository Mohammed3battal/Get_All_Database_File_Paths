## Script: List_All_Database_File_Paths.sql

**Description**:
This script returns the names and physical file paths of all database files on the SQL Server instance by querying `sys.master_files`. It includes both **data files (.mdf/.ndf)** and **log files (.ldf)** across all databases.

---

### 🔧 Query:
```sql
SELECT 
    name, 
    physical_name 
FROM sys.master_files;
```

---


### Use Case:
- Audit where data and log files are physically stored
- Prepare for database migration or file relocation
- Detect unusual or outdated file locations
- Validate consistency in storage paths (e.g., standard folder structure)


