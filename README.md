# Spotify-Data-Engineering-Project in AWS

<img width="1073" height="527" alt="image" src="https://github.com/user-attachments/assets/b0758167-4327-4347-afa3-4dfd05714e09" />


1. Raw data uploaded to S3 staging bucket
2. AWS Glue ETL transforms/processes the data
3. Processed data stored in another S3 bucket (data warehouse layer)
4. Glue Crawler scans the processed files
5. Athena creates/query tables from crawler metadata
6. QuickSight visualizes insights
