---
date: 2024-05-02
tags:
    - fact
hubs:
    - [[python]]
    - [[bigquery]]
url:
    - https://cloud.google.com/python/docs/reference/bigquery/latest/google.cloud.bigquery.client.Client#google_cloud_bigquery_client_Client_load_table_from_uri
---
# Bigquery Load From Gcs

This is a snippet for loading a `BigQuery` table from a file in `GCS` but with my own spin on it

```python
uri = Config.Storage.GIS_ACX_GRID_URI

logging.info(f"Generating schema from {PostGis.__name__}")
schema = self.bq_client.schema_from_json(PostGis.to_schema())

job_config = bigquery.LoadJobConfig(
    schema=schema,
    skip_leading_rows=1,
    source_format=bigquery.SourceFormat.CSV,
    create_disposition=bigquery.CreateDisposition.CREATE_IF_NEEDED,
    write_disposition=bigquery.WriteDisposition.WRITE_TRUNCATE,
)

logging.info(f"Loading the {Config.BigQuery.ACX_GIS_GRID_ID} table from {uri}")
load_job = self.bq_client.load_table_from_uri(
    source_uris=uri,
    destination=Config.BigQuery.ACX_GIS_GRID_ID,
    job_config=job_config,
)

try:
    load_job.result()
except Exception as e:
    print("Error", e)
    logging.error(
        f"Error in loading the table {Config.BigQuery.ACX_GIS_GRID_ID}: {e}"
    )
    raise e
```

Using a `dataclass` with a `to_schema` method I can load a table.
