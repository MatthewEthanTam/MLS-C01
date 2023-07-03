# MLS-C01
AWS Machine learning notes

## AWS Data Engineering

### Amazon S3

- allows people to store `objects` (`files`) in "`buckets`" (`directories`).

- `buckets` (`directories`) must have a `globally unique name`.

- `objects (files)` have a `key` `(full path)`

- `max` object size is `5TB`

- `object Tags` (key-value pairs) can be used for `security`, `lifecycle management`, and `storage analysis`.

- any file format can be stored in `S3` (e.g. `CSV`, `JSON`, `ORC`, `Avro`, `Parquet`, and `more`).

### Amazon Athena

- `serverless` service that allows you to `query` data in `S3` using `SQL`.

- `schema` on `read` (no `ETL` required)

- `pay per query` (no `infrastructure` to manage)

- `supports` `CSV`, `JSON`, `ORC`, `Avro`, `Parquet`, and `more`.

- Data partitioning is supported (e.g. `S3://bucket/year=2019/month=12/day=31/`)

### Amazon Glue

- `serverless` `ETL` service that allows you to `clean`, `transform`, and `normalize` data.

- `pay for what you use` (no `infrastructure` to manage)

- Does data partitioning (e.g. `S3://bucket/year=2019/month=12/day=31/`)

### S3 Storage Classes

- `S3 Standard` - availability: `99.99%`, durability: `11 9's`, latency: `millisecond`,availability SLA: `99.9%`, replicated across: `3` `AZ's`.(Frequently accessed data.)

- `S3 Infrequent Access` - availability: `99.9%`, durability: `11 9's`, latency: `milliseconds`, availability SLA: `99%`, replicated across: `3` `AZ's`. (Data accessed less frequently, but requires rapid access when needed.)

- `S3 One Zone Infrequent Access` - availability: `99.5%`, durability: `11 9's`, latency: `milliseconds`, availability SLA: `99%`, replicated across: `1` `AZ`. (Data accessed less frequently, but requires rapid access when needed. Or data you can recreate.)

- `S3 Glacier Instant Retrieval` - availability: `99.99%`, durability: `11 9's`, latency: `milliseconds`, availability SLA: `99.9%`, replicated across: `3` `AZ's`, minimum storage duration: `90 days` . (Data archived and requires retrieval within `1 minute`.)

- `S3 Glacier Flexible Retrieval` - availability: `99.99%`, durability: `11 9's`, latency: `milliseconds`, availability SLA: `99.9%`, replicated across: `3` `AZ's`, minimum storage duration: `90 days`. (Data archived and requires retrieval within Expidited (1-5 minutes), Standard (3-5 hour), and Bulk (5-12 hours).)

- `S3 Glacier Deep Archive` - availability: `99.99%`, durability: `11 9's`, latency: `milliseconds`, availability SLA: `99.9%`, replicated across: `3` `AZ's`, minimum storage duration: `180 days`. (Data archived and requires retrieval within `12 hours` (Standard) and `48 hours` (Bulk).)

- `S3 Intelligent Tiering` - availability: `99.9%`, durability: `11 9's`, latency: `milliseconds`, availability SLA: `99%`, replicated across: `3` `AZ's`. (Data that has unknown or changing access patterns. Monthly monitoring fee and auto-tiering fee)
