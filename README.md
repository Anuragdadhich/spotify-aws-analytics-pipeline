
raw
Readme · MD
# Spotify AWS Analytics Pipeline
 
Data engineering pipeline built on AWS as a beginner project.
Analyzes Spotify dataset (albums, artists, tracks) using a serverless stack.
 
**Total cost: $0 | Built in: 1 day | Level: Beginner**
 
---
 
## Architecture
 
```
albums.csv (76.3 MB)  ─┐
artists.csv (1.7 MB)   ├─→ S3 (Data Lake) → AWS Glue (ETL) → Athena (SQL) → QuickSight (Dashboard)
track.csv (10.6 MB)   ─┘
```
 
---
 
## AWS Services Used
 
| Service | What I used it for |
|---|---|
| Amazon S3 | Data lake — stored raw CSV files (88.6 MB total) |
| AWS Glue | ETL pipeline — joined album + artist + track tables visually |
| Amazon Athena | SQL queries on S3 files — no database server needed |
| Amazon QuickSight | Dashboard — bar charts, donut chart, K-pop genre analysis |
| AWS IAM | Permissions — AmazonAthenaFullAccess policy |
 
---
 
## Screenshots
 
### S3 Data Upload
![S3 Upload](screenshots/s3-upload.png)
 
### Glue ETL Pipeline
![Glue Pipeline](screenshots/glue-pipeline.png)
 
### Athena SQL Query Results
![Athena Query](screenshots/athena-query.png)
 
### QuickSight Dashboard — Followers by Album
![Dashboard 1](screenshots/quicksight-bar.png)
 
### QuickSight Dashboard — Genre Distribution (K-pop included)
![Dashboard 2](screenshots/quicksight-donut.png)
 
---
 
## What I Learned
 
- **Athena is surprising** — you can run SQL queries directly on CSV files in S3 without any database server
- **Glue visual editor** makes ETL pipelines easy to understand as a beginner
- **IAM permissions** need to be set correctly before anything works — learned this the hard way
- **QuickSight** connects to Athena in a few clicks and builds charts immediately
---
 
## Dataset
 
Spotify public dataset — albums, artists, and tracks CSV files.
88.6 MB total across 3 files.
 
---
 
## Next Steps
 
- [ ] Add Kinesis Firehose for real-time data streaming
- [ ] Set up SNS email alerts for data anomalies
- [ ] Add CloudWatch monitoring dashboard
- [ ] Pass AWS CLF-C02 certification exam
---
 
## Author
 
**Anurag Dadhich**
Cloud developer learning AWS | Jaipur, India
[LinkedIn](https://www.linkedin.com/in/anurag-dadhich-b33087223/)
 
*AWS Cloud Practitioner Essentials — completed June 2026*
