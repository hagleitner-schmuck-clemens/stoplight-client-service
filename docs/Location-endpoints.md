
NON-NESTED TYPED APPROACH
=========================

Getting a single location (typed), used for PATCH, PUT, GET

```json
/buildings/{id}
/floors/{id}
/buildingareas/{id}
/floorareas/{id}
/rooms/{id}
```

Endpoints for creating new resource, used for POST and GET

```json
/buildings/{id}/building-areas/
/buildings/{id}/floors/
/floors/{id}/floor-areas
/buildingareas/{id}/floors/
/floorareas/{id}/rooms/
```

UNTYPED APPROACH
================

Retunrns only the Base-Class elements of each location type. Can be used for GET/PUT/PATCH/CREATE?

```json
GET /customer/{id}/locatios?name=abc&type=floor,parentId=?? : query the locations of a customer with query parameters
/locatios/{lid} : get a single generic location
/locatios/{lid}/sub-locations/ : get generic sub-locations/
/location/{lid}/locations-on-path/ :get generic locations from the root to the given location
```


Whole Tree
==========
Getting the whole tree for a customer
`/customer/{id}/location-tree/ GET, PUT`

Getting all rooms for a customer
`/customer/{id}/rooms`


Getting  a single typed location NON-NESTED WITH LOGICAL GROUPING
```json
/locations/buildings/{id}
/locations/floors/{id}
/locations/buildingareas/{id}
/locations/floorareas/{id}
/locations/rooms/{id}
```
