# Spotify-Data-Engineering-Project in AWS

PIPELINE

<img width="1073" height="527" alt="image" src="https://github.com/user-attachments/assets/b0758167-4327-4347-afa3-4dfd05714e09" />


1. Raw data uploaded to S3 staging bucket
2. AWS Glue ETL transforms/processes the data
3. Processed data stored in another S3 bucket (data warehouse layer)
4. Glue Crawler scans the processed files
5. Athena creates/query tables from crawler metadata
6. QuickSight visualizes insights


## Amazon S3 Bucket Creation

Created an Amazon S3 bucket named `spotify-project-dataengineering` to serve as the centralized cloud storage layer for the data engineering pipeline. Two separate folders, `staging/` and `datawarehouse/`, were created inside the bucket to organize raw and transformed datasets efficiently.

---

## Staging Layer in S3

Uploaded raw Spotify datasets (`albums.csv`, `artists.csv`, and `track.csv`) into the `staging/` folder of the S3 bucket. This staging layer acts as the initial data ingestion zone where unprocessed CSV files are stored before ETL transformation.

---

## Data Warehouse Layer in S3

After ETL processing using AWS Glue, the transformed datasets were stored in the `datawarehouse/` folder in optimized Parquet format with Snappy compression. This layer serves as the analytical storage zone for efficient querying and downstream analytics using Athena and QuickSight.
