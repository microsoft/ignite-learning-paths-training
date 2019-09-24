# Slide 23 - Enabling Application Insights in your Application


## Part 1 - SPA Application

* Clone [https://github.com/microsoft/TailwindTraders-Website/](https://github.com/microsoft/TailwindTraders-Website/) on your local machine.
* Have VS Code open the following tabs:
  - Tab 1: `package.json` found in `.\Source\Tailwind.Traders.Web\ClientApp\package.json`.
  - Tab 2: `telemetryClient.js` found in `.\Source\Tailwind.Traders.Web\ClientApp\src\services\telemetryClient.js`
  - Tab 3: `App.js` found in `.\Source\Tailwind.Traders.Web\ClientApp\src\App.js`
  - Tab 4: `configService.js` found in `.\Source\Tailwind.Traders.Web\ClientApp\src\services\configService.js`
* Open terminal (CTRL-\`) and paste `npm i --save @microsoft/applicationinsights-web` already typed (do not press ENTER)

> We're going to show how Tailwind Traders can instrument their web applications to be able to monitor for usage insights as well as performance issues.
> We're going to start by create an instance of Application Insights within our Azure Resource Group. You'll see that we've already got this deployed here.

* Go to `FRONTEND_RESOURCE_GROUP` from variables.txt, select the App Insights Instance and go into the overview area
* Bring attention to `Instrumentation Key` on the overview blade as this is what we're going to need soon after.
* Mention that we're going to pull our code from [https://github.com/microsoft/TailwindTraders-Website/](https://github.com/microsoft/TailwindTraders-Website/)
* Open Code to our first tab `package.json` with the terminal already opened
* Talk about how the application is a .NET Core that is hosting a SPA using React and it's mostly a SPA application
* Bring attention to the line in the terminal as what we need to run to install the basics
* Jump to `telemetryClient.js`.
  - Boiler plate code to allow us to integrate Application Insights and React
  - Mention our 2 imports
  - Talk about how we are configuring it using the Application Insights Instrumentation Key (Line 13) we saw earlier
  - We now need to set our application
* Jump to `App.js`
  - Line 13 through 22 talk about how we hook AppInsights to React. Again, boilerplate code.
* Jump to `configService.js`
  - The last thing we need to do is to set our Instrumentation Key from Azure which is done here by exposing a configuration URL within .NET Core. (Line 44)

## Part 2 - .NET Core Application

> Since our application is a .NET Core application, we can also configure this part of the application easily by going directly into the Azure Portal.

* Go to the Azure Portal [https://portal.azure.com/?feature.customportal=false](https://portal.azure.com/?feature.customportal=false)
* Open the Resource Group `FRONTEND_RESOURCE_GROUP` from variables.txt
* Open the Australia East Front-end `tailwindtraders-website-auseast-apps50-*`
* Open Application Insights from overview window. Note that you can also open it from the left blade under `Settings`
* Application Insights should already be configured. Talk about what we can track and how it doesn't require any kind of boilerplate code.
  - What is being tracked is in a list under `Instrument your application > .NET`
* Talk about how the only thing that needs to be done is to flick the switch to enable
* Bring attention to the language choices and the documentation links on how to enable them
* Open back the `tailwindtraders-appinsights-apps50-*` resource on the overview tab.

> Once everything is enabled, telemetry starts to get collected and that opens scenarios that allow us to better understand our application.

* Open the `Investigate > Application map` tab. Talk about how it allow us to track what services our frontend is interacting with.
* Open the `Investigate > Smart Detection` tab. Click on settings and talk about what kind of events we can be notified about:
  - Performance issues
  - Trace severity ratio
  - Abnormal rise in exceptions
  - Memory leaks
  - Security issues like Insecure urls, insecure forms, suspicious user activity
  - Sudden rise in traffic (monitor app cost )
  
* Open the `Investigate: Live Metrics Stream`
  - Talk about how when interacting with the app, you start getting realtime information about every requests and events.

> Now that we are equiped with all of this tooling, we're ready to start understanding the root cause of our issues.
