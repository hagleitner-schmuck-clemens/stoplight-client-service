* GUID AND Int as PK
* Return for  POST PUT, PATCH 
  * Return the resoruce: Includes IDs and other autocalculated properties like last change date etc. seems preferable
  * Return just the auto generated Id: CLient can decide if he needs the object.
  * Use 204 Result if no data is returned.


* Rate limit (e.g. when self-registering with a customer)  5 / Second

https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
https://docs.microsoft.com/en-us/dotnet/api/microsoft.odata.uriparser.orderbyclause.expression?view=odata-core-7.0
https://www.odata.org/documentation/odata-version-2-0/uri-conventions/
https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design
https://github.com/microsoft/api-guidelines/blob/master/Guidelines.md