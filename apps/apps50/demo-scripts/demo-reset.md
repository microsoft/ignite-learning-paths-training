# Reset to initial state

## Front-End

* We're working with the Resource Group `pdecarlo-apps50-frontend`.
* Ensure all AppService in that group are started
* Ensure that Azure Front Door backend pools points to `tailwindtraders-website-auseast-apps50` and `tailwindtraders-website-eastus-apps50`.
* When you go to [http://tailwind-apps50.azurefd.net](http://tailwind-apps50.azurefd.net), note the name of the region in the header (Australia East/East US).

  - If `East US`, use the `tailwindtraders-website-eastus-apps50` AppService.
  - If `Australia East`, use the `tailwindtraders-website-auseast-apps50` AppService

  - For the AppService that display on Azure Front Door
    * Go to Configuration, ensure that `ApiUrl` is set to `http:///webbff/v1`
    * For the other AppService, ensure that `ApiUrl` is set to `http://ebc0eece880b482d91a7.eastus.aksapp.io/webbff/v1`
* Make sure you have `az aks browse -g pdecarlo-apps50-backend -n tailwindtradersaks56ime2uif7zxk` running in a console. If it's not running, make sure it's in the history for easy access.
* Set the `Config Maps` for `cfg-my-tt-cart-cart-api`. Ensure `HOST` is empty.

## Back-end

TODO