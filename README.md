# <a name="_khu82qlpyqzn"></a>**CloudTunes - Spotify ETL Pipeline**
This project focuses on building an automated pipeline to extract, transform, and load personalized Spotify playlist data into Amazon S3 for analytical purposes.
## <a name="_mfymi4aqp582"></a>**Overview**
The pipeline extracts weekly listening data from the Spotify API using the Spotipy Python library. This raw JSON data gets transformed into analysis-ready CSV datasets structured around songs, albums, and artists. Further processing happens via AWS services like Lambda, Glue, Athena to enable automated workflows and simplified SQL querying.

The goal is to maintain always up-to-date Spotify data that can provide insights into user listening patterns.
## <a name="_vfoa18qfshjp"></a>**Architecture**

The main components are:

- Data Extraction - Spotify API integration via Spotipy to collect playlist data
- Transformation - Lambda functions to process & transform JSON data into CSVs
- Orchestration - EventBridge schedule and triggers to automate pipeline
- Storage - S3 buckets to store raw, intermediate and transformed data
- Metadata - AWS Glue crawlers to catalog dataset schema
- Analysis - Query transformed data with Athena SQL
## <a name="_xc2hso25b26u"></a>**Implementation Details**
Key steps:

- Set up Spotify API credentials
- Create S3 buckets
- Python ETL scripts for data extraction and transformation
- Lambda functions to deploy ETL logic
- EventBridge triggers to activate scripts on schedules/events
- Output transformed datasets partitioned by songs, albums, artists
- Glue crawlers infer schema and populate Metadata Catalog
- Athena configured to run SQL queries on processed data
## <a name="_9918s34u70he"></a>**Getting Started**
Prerequisites:

- Spotify developer account
- AWS environment with access keys
- Python, AWS CLI/SDK

Key steps:

1. Register Spotify app to obtain API credentials
1. Configure S3 buckets
1. Develop ETL logic in Python
1. Deploy Lambda functions for pipeline stages
1. Set up EventBridge triggers
1. Activate Glue crawlers to crawl data
1. Start querying with Athena SQL
## <a name="_1psm2npov8a1"></a>**Next Steps**
Future enhancements:

- Enrich datasets with more attributes
- Build visualization dashboards
- Logging, monitoring, alerts
- Workflow orchestration tools
- Containerization and CI/CD

