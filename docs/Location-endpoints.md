
NON-NESTED TYPED APPROACH
=========================

Getting a single location (typed) NON-NESTED used for PATCH, PUT, GET
/buildings/{id}
/floors/{id}
/buildingareas/{id}
/floorareas/{id}
/rooms/{id}

Endpoints for creating new resource NON-NETED used for POST and GET
/buildings/{id}/building-areas/
/buildings/{id}/floors/
/floors/{id}/floor-areas
/buildingareas/{id}/floors/
/floorareas/{id}/rooms/

UNTYPED APPROACH
================

Retunrns only the Base-Class elements of each location type. Can be used for GET/PUT/PATCH/CREATE?

Returns generic locations: NESTED

GET /customer/{id}/locatios/{lid} : list all children
/customer/{id}/locatios/{lid}/sub-locations/

GET /customer/{id}/locatios?name=abc&type=floor,parentId=?? : query the locations of a customer with query parameters
/locatios/{lid} : get a single generic location
/locatios/{lid}/sub-locations/ : get generic sub-locations/
/location/{lid}/locations-on-path/ :get generic locations from the root to the given location


Whole Tree
==========
Getting the whole tree for a customer
/customer/{id}/location-tree/ GET, PUT

Getting all rooms for a customer
/customer/{id}/rooms


Getting  a single typed location NON-NESTED WITH LOGICAL GROUPING
/locations/buildings/{id}
/locations/floors/{id}
/locations/buildingareas/{id}
/locations/floorareas/{id}
/locations/rooms/{id}
