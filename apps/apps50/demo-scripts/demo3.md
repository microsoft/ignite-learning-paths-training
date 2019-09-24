# Slide 25 - Finding and Fixing Failures with Failure Analysis in Application Insights

* Remind users of what happened in the first demo `Identifying the issue`.
* Using the values in your variables.txt file, compare both endpoints `AUSTRALIA_EAST_SITE` and `EAST_US_SITE` 
  - For each, click on Powertools category
* For the failing endpoint, open the F12 tools in a Chromium-based browser and go to the `Network` tab and hit F5 again.
* Bring attention to `?&type=diytools` request that hits `http://AKS_BACKEND_ENDPOINT/webbff/v1/products?&type=diytools`. 

> Let's go see what it looks like inside AppInsights

* Open the AppInsights within the frontend `tailwindtraders-appinsights-apps50`
* Navigate to the Application Map. Notice the `webbff` endpoint which is not a valid domain.
* Click on the `webbff` node, then `Investigate failures` on the right
* Notice all the failed requests around `webbff`
* Click **on the number** of the first line in the top 10 response. Mention the suggested query to debug.
* Click the suggested query to debug
* Click on the line where `?&type=diytools` fails. Talk about the elements on the right. Especially the url with a  `http://AKS_BACKEND_ENDPOINT/webbff/v1/`. 

> Note how this looks like it might be a configuration issue.

* Go back to Resource Group `FRONTEND_RESOURCE_GROUP` from variables.txt
* Go to the AppService exhibiting the issue (Australia East/EastUS)
* Go to `Settings > Configuration`
* Show value of `ApiUrl` and `ApiUrlShoppingCart`.
* Mention that `ApiUrl` and `ApiUrlShoppingCart` are basically missing the proper host.  Replace the "http://AKS_BACKEND_ENDPOINT" portion of both `ApiUrl` and `ApiUrlShoppingCart` using the value from `AKS_BACKEND_ENDPOINT` in variables.txt to fix the issue. **Save** and restart the App Service instance
* Go back to the failing website. Force refresh the page. Navigate back to the PowerTools section. 
* Everything should work
* Summarize what we have just done.
