# n8n Sales Data Pipeline

An automated sales data pipeline built with n8n as part of the n8n Foundations course.

## What it does

This workflow automatically:

1. Retrieves sales data from an API
2. Splits 50 orders into individual records
3. Calculates order totals
4. Sends processed orders to an operations endpoint
5. Filters delivered orders
6. Generates regional sales summaries
7. Validates the regional analysis
8. Adds report metadata
9. Converts the results into a CSV file
10. Sends the final report to the reporting endpoint

## Workflow Architecture

TriggerManual
↓
GetSalesData
↓
SplitOrders
↓
SetOrderTotals
├── AggregateOrders → SendOrders
│
└── FilterDelivered
↓
SummarizeByRegion
↓
UpdateFieldNames
├── AggregateRegions → SendAnalysis
│
└── SetReportMetadata
↓
ConvertToCSV
↓
SendReport

## Technologies

- n8n
- REST APIs
- HTTP Request
- JSON
- Expressions
- Data Transformation
- Conditional Branching
- Aggregation
- CSV Generation

## Key Concepts Demonstrated

- Header Authentication
- API Integration
- Split Out
- Edit Fields
- IF conditions
- Summarization
- Aggregation
- Branching
- Binary File Handling
- CSV Report Generation

## Project Result

The workflow processes sales data, analyzes delivered orders by region, and generates a structured CSV report automatically.

## Note

This project was created as part of hands-on n8n automation learning.
Credentials, API keys, and personal assessment information have been removed from the published workflow.
