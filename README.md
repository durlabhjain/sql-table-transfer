# Overview

A simple nodeJS utility to transfer one MS-SQL table to another database on same or another server.

The utility assumes BCP tools are installed and are in path.

# Configuration

Copy .config.json to .config.local.json and then specify your connection strings as desired.

# Usage

```
node index.mjs --src source:sampleTable --dest target:sampleTable --batchSize 10000 
```

Here:
--src           source:sampleTable source is the name of connectionString and sampleTable is the source table name
--dest          target:sampleTable target is the name of connectionString and sampleTable is the destination table name
--batchSize     Set bcp batchSize


# Limitations

Following SQL table specs are not maintained/ handled:
1. Primary Key
2. Unique constraints
3. Calculated columns
4. Indexes
5. Relationships
6. Collation

Not tested against different variations