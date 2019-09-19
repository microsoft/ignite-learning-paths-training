# Taking Your App to the Next Level with Monitoring, Performance and Scaling

## Deployment

First you will need to [deploy the Tailwind Traders Reference Deployment to an AKS instance](https://github.com/neilpeterson/tailwind-reference-deployment#tailwind-traders-aks).  Be sure to select the "Deploy to Azure" button that is under the "Tailwind Traders AKS" heading.  Follow the instructions in the README of the above linked repo to obtain the url of the newly deployed Tailwind Traders website, we will refer to this url in the next section as the `{AKS_BACKEND_ENDPOINT}`

Next, you will need to deploy the Apps50 specific resources provided by the "Deploy to Azure" button below:
[![Deploy to Azure](https://azuredeploy.net/deploybutton.svg)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftoolboc%2Fignite-learning-paths-training%2Fapps50deployment%2Fapps%2Fapps50%2Fdeploy%2Fdeployment.json)

You will need to provide values for the following three parameters:
![](./assets/settings.png)

`Resource Name Suffix` is a value that is appended to the end of all created resources, ex: if you were to put "deployment" here, it would create the following resources:

![](./assets/resources.png)

You will also need to update the `{AKS_BACKEND_ENDPOINT}` portion of `Api Url` and `Api Url Shopping Cart` with the value obtained when deploying the Tailwind Traders Reference Deployment to an AKS instance.

The deployment can take up to 20 minutes to complete.  When it is finished you should see a set of resources similar to the picture above deployed into the resource group that you selected.

## Demos

To reset the demo, please refer to the [reset instructions](./demo-scripts/demo-reset.md).

The demos are set to but run in the following order:

* [Identifying the issue](./demo-scripts/demo1.md)
* [Enabling Application Insights in your Application](./demo-scripts/demo2.md)
* [Finding and Fixing Failures with Failure Analysis in Application Insights](./demo-scripts/demo3.md)
* [Monitoring and Fixing Failures in AKS using Azure Monitor for Containers](./demo-scripts/demo4.md)
 