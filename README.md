# OcStore3Utf8mb4
Change DB encoding to utf8mb4 (ocStore 3.0.3.7)

1. Convert tables. Use this snippet to get commands for all tables:
`SELECT CONCAT('ALTER TABLE "', TABLE_NAME,'" CONVERT TO CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci, ROW_FORMAT = DYNAMIC;') AS mySQL
FROM INFORMATION_SCHEMA.TABLES
WHERE TABLE_SCHEMA= "%ИМЯ_БАЗЫ%"
AND TABLE_TYPE="BASE TABLE"`
2. Install following .ocmod.zip
3. Flush system cache
