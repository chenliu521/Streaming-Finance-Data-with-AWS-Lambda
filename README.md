# Streaming-Finance-Data-with-AWS-Lambda
is focuses on building a real-time data pipeline for finance data records using AWS Lambda. The pipeline involves data collection, analysis, and visualization to enable interactive querying and provide insights into the streaming data.

This project leverages AWS services, including Lambda, Kinesis, Glue, and Athena, to create a real-time data pipeline for finance data records. The Lambda function collects stock price data using the yfinance module and pushes it to the Kinesis stream. The data is then stored in S3 and made available for interactive querying and analysis using AWS Athena. 
Finally, visualizations are generated based on the query results to provide insights into the average volatility trend and daily highest volatility per company.

screenshot_of_s3_bucket.png
# <img width="468" alt="image" src="https://github.com/chenliu521/Streaming-Finance-Data-with-AWS-Lambda/assets/71107771/7faf54bb-7fe6-4866-add7-4d38098833cf">

## Collects the data from yfinance and puts it into the firehose stream on S3 bucket
kinesis_monitor.jpeg
# <img width="468" alt="image" src="https://github.com/chenliu521/Streaming-Finance-Data-with-AWS-Lambda/assets/71107771/1282441e-5bd6-4702-bc64-14570aa0b53d">

## AWS Kinesis configuration page
exec_results.jpeg
# <img width="468" alt="image" src="https://github.com/chenliu521/Streaming-Finance-Data-with-AWS-Lambda/assets/71107771/ca82db1f-859b-4794-9be1-d4325b6a72ff">

## Data is collected via Lambda Function
results.jpeghe query is run through AWS Athena）
# <img width="468" alt="image" src="https://github.com/chenliu521/Streaming-Finance-Data-with-AWS-Lambda/assets/71107771/7ffe65a0-a367-4960-b135-92cd1445bc59">

# Data Visualization
## 1)	Graph the average volatility trend per company (A single Line Chart: Each line refers to a company)
Which company is the most volatile?
# <img width="330" alt="image" src="https://github.com/chenliu521/Streaming-Finance-Data-with-AWS-Lambda/assets/71107771/8f83d168-1f2d-4801-b157-5c9541b513f4">
As you can see from Average volatility trend per company, company COST is the most volatile company, and the average volatility number is 0.683444.

## 2)	Graph the daily highest volatility per company (A Grouped Bar Chart: Each group refers to a company and the bars refer to the daily highest volatility)
Do the findings from this graph support your conclusion from the first graph?
# <img width="374" alt="image" src="https://github.com/chenliu521/Streaming-Finance-Data-with-AWS-Lambda/assets/71107771/db3bee6d-74e8-466c-8733-7936d4dee820">

Company COST exhibited the highest daily volatility, reaching approximately 5 on April 6, 2023. The second-highest daily volatility was observed on April 11, 2023, with a value of around 4.
TGT had a daily highest volatility of approximately 2.5, while WMT recorded a daily highest volatility of approximately 2. Both TGT and WMT experienced their highest volatilizes on the same day as COST.

Therefore, these findings in the second chart are consistent with the conclusion reached in the first chart, which identifies COST companies as the most volatile companies based on the highest average volatility.






