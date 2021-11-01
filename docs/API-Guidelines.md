### Roadmap
* 2021-11-03 (Version alpha.01): All relevant endpoints for CWS are described, API design is syntactically correct.
* 2021-11-17 (Version beta.01): Includes outcome of HAG developer review, open design questions resolved, consistent and well documented API. 
* 2021-11-24 (Version rc.01): Includes outcome of CWS developer review, basis for starting development at CWS.

### Open API design questions
* GUID AND Int as PK
* Return for  POST PUT, PATCH 
  * Return the resoruce: Includes IDs and other autocalculated properties like last change date etc. seems preferable
  * Return just the auto generated Id: Client can decide if he needs the object. Not suitable for resoruces whith multiple auto-calculated data fields.
  * Fire and forget: In some usecases (e.g. controller endpoints). Use 204 Result if no data is returned.
* Rate limit, and rate limit advertadvertising  (e.g. when self-registering with a customer) 
* Pagination link-header, X-Total-Count
* orderBy expression based on ODATA? https://docs.microsoft.com/en-us/dotnet/api/microsoft.odata.uriparser.orderbyclause.expression?view=odata-core-7.0
* comparison espression for filters? standards?

### References for API design
* https://github.com/microsoft/api-guidelines/blob/master/Guidelines.md
* https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
* https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design
