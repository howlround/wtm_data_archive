# World Theatre Map Data Archive

## Data formats and usage

- In this repository you will find the data from the world threatre map exported into three formats. CSV, JSON, and a MongoDB snapshot.
- Records all have unique IDs that can be used to create a fuller picture of the data (using pivot tables with the CSVs or multiple queries or $lookup with the JSON for example).
- Some of the CSVs retain remnants of the original json data structure. We were not able to flatten the data in a way that made it easy to still search for data effectively. So you will need to search cells using CONTAIN, or further flatten the data to suit your needs.
- If you have the capacity to do so the mongodb snapshot will give you the full functionality of the original database.

## Restoring MongoDB Snapshot

- The tar.gz file inside the mongodb-snapshot directory can be expanded placed in the `data` directory of a local mongodb installation.
- The database uses the legacy mmapv1 storage engine.
- You have to use a version of MongoDB prior to 4.2 and use the `--storageEngine=mmapv1` flag when starting mongo.
