### Processlist
```sql
SELECT * FROM pg_stat_activity;
```

### Kill process
```sql
SELECT pg_cancel_backend(2745635);
```
