# Database_Freshness_Anomaly_Detection

We collects the last update time for each table on an hourly basis and uses it
for detection of data freshness issues. The attached CSV file contains table
update times inferred from this data, with the below schema.

Each table’s updates can be thought of as a unique time-series. We aim to provide to the client at each inference run of our model a list of tables which
are currently experiencing issues. Since alert fatigue is a major concern we also prioritize Precision over Recall.

Steps:
1.Create a precision focused simple model, allowing detection of the most clear cut
table freshness issues. For this v0 model, having very low recall is fine, we only
need a handful of examples.
2. Evaluate ways to improve the accuracy of your V0 model.
3. Implement an upgraded version v1 
