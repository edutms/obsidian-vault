2025-07-30 09:16

### Status: #baby

### Tags: [[AWS]] [[machine-learning]]

# What is Amazon Comprehend?
Amazon Comprehend is Amazon's NLP solution for text-based documentation, capable of [[Name Entity Recognition]], [[Sentiment Analysis]]. language detection, PII Redaction and more NLP-based solutions. It's useful with text based documents only, so if you intend using it for PDF document analysis it's commendable to use first a text-extraction solution such as [[Amazon Textract]] or open-source Python libraries such as [PyPDF2](https://pypi.org/project/PyPDF2/) ]

## Examples


## Pricing 
For this current project ideally it would be using Topic Modeling. This method identifies relevant terms, topics from the documentation already stored in S3. It will identify the most common topics in the collect and organize it in groups belonging to which topic.
### Custom entities and classification

| Desc                                                       | $                                                           |
| ---------------------------------------------------------- | ----------------------------------------------------------- |
| Entity recognition with PDF, Word and plain text documents | 0,0005 per unit (100 chars, minimum of 3 units per request) |
| Model training                                             | 3 per hour                                                  |
| Model management                                           | 0,5 per month                                               |
|                                                            |                                                             |
There is a free tier of 50k units of text - five million characters per month.

From AWS Comphend [pricing guide](https://aws.amazon.com/comprehend/pricing/?pg=ln&sec=hs):
####  Example 8 – Extracting mortgage application entities using the custom entity API

Let us say you want to train a custom entity extraction model to extract 10 custom entities from a mortgage application. One hundred customers apply every day, each providing a 10-page scanned PDF document containing 2,500 characters per page. Using Amazon Textract, let’s assume we need to extract the text from every single page processed before extracting entities using Detect Document Text API. It takes one hour to train the custom model, and you are planning to keep this model for a month. So, model training costs will be $3 and model storage costs will be $0.50 for the month. Let us also assume that you are in the second year of your use of the service and are not eligible for the free tier offering. To extract custom entities asynchronously you pay by number of characters in your documents. To extract entities in real time you provision an endpoint with enough throughput to handle your use case and pay for the time that the end point is up.

**Inference cost calculation for asynchronous classification:**

Size of each request per day = 2,500,000 characters [100 applications/day * 10 docs * 2,500 characters]

Number of units per request = 25,000 units [2,500,000 characters ÷ 100 character per unit]

Price per unit = $0.0005

Total inference cost for units = $12.50 [25,000 units x $0.0005]

Amazon Textract cost for Detect Document Text API= $1.50 [100 applications/day * 10 docs * $0.0015 price per page, up to 1M pages]

**Total cost = $17.50 [$12.50 inference + $1.50 Textract + $3 model training + $0.50 model storage]**






# References









