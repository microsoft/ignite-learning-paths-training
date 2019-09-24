# Slide 36 - Monitoring and Fixing Failures in AKS using Azure Monitor for Containers

> But this doesn't fix our issues. If zero sales were made, it might be another issue. From our customers, we received reports that the shopping cart stopped working. 
> That would affects all regions since our backend is hosted on AKS and is region agnostic.

* Go to any of our website directly
* Back to the powertools section
* Any item: `Add to list` then `Add to cart`
* Open the F12 tools on a Chromium browser, F5.
* Notice the `shoppingcart` failure. Mention the 0 bytes. The URL is correct this time.

> We could jump into our Kubernetes cluster directly using `kubectl` but that would require everyone to have access admin access to the cluster.
> Now let's see how we could monitor such failures directly from Azure Monitor.

* Head to Kubernetes Service located in our backend resource group `AKS_RESOURCE_GROUP` from variables.txt.
* Mention we already activated Azure Monitor for AKS. Click on `Monitor containers` on the Overview tab.
* Discuss about what we see (health of our nodes, node count, active pods, etc.)
* Mention the active pods blip in the `Active Pods` graph
* Mention that you can drill from Cluster, to nodes, to controllers, all the way down to Containers
  - You can click on each of them to show a preview.
* Go to the `Containers` level
* Notice the `cart-api` container with a `Warn` and 41 restarts. Click on it.
* Notice the `Container Status Reason` being `CrashLoopBackOff`
  - This means that the container failed to start repeatedly and is now waiting on manual intervention.
* Let's debug a bit by going in the Environment Variables
* Notice the lack of `HOST` value which is what dev environment uses.
* Go in `View in analytics` and click `View container logs`
* Go through the list of all analytics. Mention the line where `Local environment detected`
* Go to our AKS cluster by the `az aks browse` command.
* Go to our `Config and Storage > Config Maps` since this is where container configurations are stored.
* Click on `cfg-my-tt-cart`. Mention that the host section is blank.
* Click on `EDIT`
* Set the `HOST` value to the value of `HOST` from variables.txt
  - This is the host for the COSMOS DB
* To restart, go to `Workloads > Pods` and delete the cart-api pod. K8S will restart the container.
* Head back to Application and test out `Add to cart`.
* Should work now

> Talk about what could be done. Send alerts, etc.

End of demo.
