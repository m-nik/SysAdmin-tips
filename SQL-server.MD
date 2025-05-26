# create user with custom SID
<https://techcommunity.microsoft.com/discussions/sql_server/creating-a-sql-login-with-sql-server-availability-groups/3736766>
```sql
USE [master]
-- on a server
SELECT [sid], [name] FROM [syslogins] WHERE [name] = 'ziture';
-- on another server
CREATE LOGIN ziture WITH PASSWORD = N'nae0haiW6voaihUob6ahlaAeyl6hMiequw1', sid=0x74C1618EDB2215478CEC4D52B34F6629;
```
