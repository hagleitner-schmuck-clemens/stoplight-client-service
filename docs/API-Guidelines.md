### Roadmap
* 2021-11-01 (Version 1.1.0-alpha.01): All relevant endpoints for CWS are described.
* 2021-11-03 (Version 1.1.0-alpha.02): All relevant endpoints for CWS are described, API design is syntactically correct.
* 2021-11-17 (Version 1.1.0-beta.01): Open design questions resolved, developer input included, consistent and well documented API. 
* 2021-11-24 (Version 1.1.0-beta.02): Includes outcome of CWS developer review, basis for starting development at CWS.
* 2022-01-31 (Version 1.1.0-rc.01): Includes outcome of CWS developer review, basis for starting development at CWS.
* 2022-03-31 (Version 1.1.0): Final version no breaking changes.

All versions will be tagged in Git.


### Open API design questions
* GUID AND Int as PK
* Return for  POST PUT, PATCH 
  * Return the resoruce: Includes IDs and other autocalculated properties like last change date etc. seems preferable
  * Return just the auto generated Id: Client can decide if he needs the object. Not suitable for resoruces whith multiple auto-calculated data fields.
  * Fire and forget: In some usecases (e.g. controller endpoints). Use 204 Result if no data is returned.
* Can we infer the HsM User-ID from any HTTP request? (i.e. for controller endpoints /customer/{id}/mark-favorite, /customer/{id}/mark-recently-used)
* Rate limit, and rate limit advertadvertising  (e.g. when self-registering with a customer) 
* Pagination link-header, X-Total-Count
* orderBy expression based on ODATA? https://docs.microsoft.com/en-us/dotnet/api/microsoft.odata.uriparser.orderbyclause.expression?view=odata-core-7.0
* comparison espression for filters? standards?

### References for API design
* https://github.com/microsoft/api-guidelines/blob/master/Guidelines.md
* https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
* https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design