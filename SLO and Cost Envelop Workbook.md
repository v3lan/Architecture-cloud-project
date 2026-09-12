

|**Metric**|**Metric Name**|**Target Objective**|**Meaning**|
|-|-|-|-|
|Availability SLI|Uptime Percentage|99.9% per month|Service can only be down for a max of \~43 minutes per month.|
|Latency SLI|Response Time|95% < 200ms|95 out of 100 requests must respond faster than 200 milliseconds.|
|Error Budget|Allowed Failure|0.1%|The allowable percentage of total requests that can fail.|
|Paging Threshold|Emergency Alert|>2% error rate over 5 min|Triggers an immediate notification to the engineer on call.|





**Cloud Cost Envelop Model**



|Infrastructure Component|Scenario A: Low (1k req/day)|Scenario B: Medium (100k req/day)|Scenario C: High (10M req/day)|
|-|-|-|-|
|Compute (API Tier)|$0 (Free Tier)|$15/month|$120/month|
|Database (Storage \& DB)|$0 (Free Tier)|$25/month|$150/month|
|Network Data Transfer|$|$5/month|$45/month|
|Logging \& Monitoring|$ (Free Tier)|$10/month|$60/month|
|Backups \& Snapshots|$|$2/month|$20/month|
|Support Tier|$ (Basic Free)|$0 (Basic Free)|$100 (Developer/Business)|
|Estimated Total Cost|$0/month|-$57/month|-$495/month|



