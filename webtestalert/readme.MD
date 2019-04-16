# webtestalert
[![Deploy to Azure](https://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fkaranotts%2Farm_templates%2Fmaster%2Fwebtestalert%2Fapp_ins_alerts.json)
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fkaranotts%2Farm_templates%2Fmaster%2Fwebtestalert%2Fapp_ins_alerts.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>


```json
"health_page": {
            "value": [
                {
                "name": "statuspage",
                "guid": "[newGuid()]",
                "url": "https://payments.statuspage.io/api/v2/status.json",
                "findText": "All Systems Operational",
                "locations": [
                    { "Id": ```json },
                    { "Id": "emea-se-sto-edge" }
                    ]
                }
            ]
        }
```
name: name for your test
guid: generated automatically
url: page you want to monitor
findText: text that must appear in the page for the webtest to pass
locations: ping locations
