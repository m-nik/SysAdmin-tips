# create user with custom SID
<https://techcommunity.microsoft.com/discussions/sql_server/creating-a-sql-login-with-sql-server-availability-groups/3736766>
```sql
USE [master]
-- on a server
SELECT [sid], [name] FROM [syslogins] WHERE [name] = 'anyname';
-- on another server
CREATE LOGIN anyname WITH PASSWORD = N'anypassword', sid=0x74C1619EDB2215835CEF4D52B34F6629;
```
