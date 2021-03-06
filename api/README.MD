# API

These sections detail the external (i.e. REST/Websocket) as well as the internal (ie Classes/Functions) [API](https://en.wikipedia.org/wiki/Application_programming_interface) of Weacast.

You might read this [introduction article](https://blog.feathersjs.com/feathersjs-in-production-configuration-api-prefixing-logging-and-error-catching-2a80e044e233) about using Feathers in production because it has been used as a guideline for the development Weacast.

> **All dates/times in Weacast are managed as [moment](https://momentjs.com) objects and expressed in [UTC](https://en.wikipedia.org/wiki/Coordinated_Universal_Time).**

* Core
  * [Application](/api/APPLICATION.MD)
  * [Forecast model](/api/FORECAST.MD)
  * [Forecast element](/api/ELEMENT.MD)
  * [Hooks](/api/HOOKS.MD)
  * [Grid](/api/GRID.MD)
* Plugins
  * [Forecast models](/api/PLUGIN.MD)
  * [Probe](/api/PROBE.MD)
  * [Alert](/api/ALERT.MD)
* Client-specific
  * [Layers](/api/LAYERS.MD)
  * [Mixins](/api/MIXINS.MD)
  
## Testing

You will find [here](./Weacast.postman_collection.json) a collection of ready-to-go REST requests to test the API with the great [POSTMAN](https://www.getpostman.com/) tool. Simply download it and import it in your POSTMAN installation.

You should do the following:
1. make your Weacast installation run (the collection is configured for default dev port `8080` but you can easily switch to `8081` for production mode for instance or any other)
2. use the authenticate request with a registered user e-mail/password to retrieve an authorization token
3. set this token in the header of other requests in order to be authorized to perform the request
4. renew your token when expired (step 2)
