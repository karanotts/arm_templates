# webtestalert
[![Deploy to Azure](https://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fkaranotts%2Farm_templates%2Fmaster%2Fwebtestalert%2Fapp_ins_alerts.json)
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fkaranotts%2Farm_templates%2Fmaster%2Fwebtestalert%2Fapp_ins_alerts.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

Required input: 

```json
"app_ins_name": {
    "value": "rdo-temp-statuspage-ai"
    }
```
app_ins_name: name for your application

```json
"health_page": {
    "value": [
        {
        "name": "MyWebPage",
        "url": "https://mywebpage.com/api/latest/status.json",
        "findText": "All Systems Operational"
        }
    ]
}
```
name: name for your test
url: page you want to monitor
findText: text that must appear in the page for the webtest to pass

```json
"queryRule":{
    "value": [
        {
        "query": "availabilityResults\n| where message contains \"Validation Rule Error\"\n",
        "actionGroup": "/subscriptions/MySubscriptionGUID/resourceGroups/MyLogAlertsSpace/providers/microsoft.insights/actionGroups/MyActionGroup"
        }
    ]
}
```
query: Log Analytics query that triggers alert
actionGroup: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/action-groups
