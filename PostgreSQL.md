Link: [[Back-end development]]
Link: [[Database]]
# Features
---
## Whole-row references
```SQL
CREATE TABLE data (id serial, person text, country text);

INSERT INTO data (person, country)   
VALUES ('Tim','France'),('Dieter','Germany'),('Marcus','Finland');

-- Create backup_data table and add data as Json data
CREATE TABLE backup_data (id serial, backup_json);
INSERT INTO backup_data (backup_json) SELECT to_jsonb(data) FROM data
```

