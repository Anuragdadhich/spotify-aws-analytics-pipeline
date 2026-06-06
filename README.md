
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


![S3 Upload](screenshots/s3-upload.png)
 
### Glue ETL Pipeline
<img width="1907" height="808" alt="Screenshot 2026-06-06 092946" src="https://github.com/user-attachments/assets/3ef5dd88-9e0b-402e-a710-449319c4d4df" />

 
### Athena SQL Query Results
<img width="1882" height="812" alt="Screenshot 2026-06-06 172638" src="https://github.com/user-attachments/assets/5aab1cc8-eb2c-4fed-867f-a0dc4d6c6d25" />
 
### QuickSight Dashboard — Followers by Album
 <img width="1906" height="832" alt="Screenshot 2026-06-06 202455" src="https://github.com/user-attachments/assets/d088c287-cd87-45db-b5c8-e919efbf6d7e" />

 
### QuickSight Dashboard — Genre Distribution (K-pop included)

<img width="1897" height="882" alt="Screenshot 2026-06-06 200406" src="https://github.com/user-attachments/assets/4949a0c3-dba0-45f4-ac2c-dccaac42dd81" />
<img width="1913" height="732" alt="Screenshot 2026-06-06 194859" src="https://github.com/user-attachments/assets/da13a874-1237-49a0-8343-1189b6968384" />
<img width="1907" height="882" alt="Screenshot 2026-06-06 185428" src="https://github.com/user-attachments/assets/81fd9574-5438-474e-b74f-0553611a0e5a" />
 
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
