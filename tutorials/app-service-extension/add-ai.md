---
Order: 5
Area: appservicetools
TOCTitle: Add App Insights
PageTitle: Add App Insights
MetaDescription: Node.js Deployment to Azure App Services with Visual Studio Code
DateApproved:git
---
# Monitor your application with Azure Application Insights

In this step, you add Azure Application Insights to your Node.js website using VS Code and the Azure App Service extension. This tutorial assumes you have deployed your site to an Azure App Service on Linux.

With Azure Application Insights, you can easily monitor your web application for availability, performance, and usage. You can also quickly identify and diagnose errors in your application without waiting for a user to report them.


## Create an Application Insights instance

During the App Service creation, you were prompted to enable Application Insights. If you chose to enable it, the following happened behind the scenes:

- An Application Insights instance was created for you
- Your application's instrumentation key was added as an application setting
- The Application Insights for Node.js npm package was installed

A new file called XXXX.txt was also created that contains the following two lines of code:

```
const appInsights = require('applicationinsights');
appInsights.setup(process.env.APPLICATIONINSIGHTSKEY).start();
```
Paste these two lines of your code at the topmost part of your script.


If you chose to skip enabling Application Insights earlier, you can configure it now. You can also deploy from the Command Palette (Ctrl+Shift+P) by typing 'add app insights' and running the Azure App Service: Add Application Insights command.

1. Create a new Application Insights instance or select an existing one
2. Enter the name of the new Application Insights instance
3. Select the location for the instance


## Monitor your application

Once Application Insights has been enabled for your application, you can view the Application Insights node created under your application.

From here you can click on "Search Telemetry" to view some of the basic metrics about your application. This enables CodeLens indicators to appear on top of public request methods in your web application. You can see CodeLens such as number of total requests, number of failed requests, average response time and number of exceptions.

You can also click on "Go to Portal" to directly visit the Application Insights resources to view more detailed dashboards and metrics.

----

<a class="tutorial-next-btn" href="/docs">I'm Done!</a> <a class="tutorial-feedback-btn" onclick="reportIssue('node-deployment-azureappservice', 'add-ai')" href="javascript:void(0)">I ran into an issue</a>