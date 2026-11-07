```sql
CREATE VIEW <view_name> AS
SELECT <column_name(s)>
FROM <table_name>
WHERE <condition>
```

```sql
CREATE VIEW dept_info(dname,budget,manager)
AS
SELECT d.dname, d.budget, e.ename 
FROM emp e, dept d
WHERE e.eid = d.managerId
```

