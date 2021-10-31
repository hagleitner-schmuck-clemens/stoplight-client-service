# Endpoints for typed locations

### Single location (PATCH, PUT, GET)

```json
/buildings/{id}
/floors/{id}
/buildingareas/{id}
/floorareas/{id}
/rooms/{id}
```
### Location collections (GET, POST)

```json
/buildings/{id}/building-areas/
/buildings/{id}/floors/
/floors/{id}/floor-areas
/buildingareas/{id}/floors/
/floorareas/{id}/rooms/
```

# UNTYPED
=========

Returns  only the Base-Class-Object of each location type. User for get

`/customer/{id}/locations?name=abc&type=floor,parentId=1234` : query the locations of one customer with various parameters `GET`

`/locatios/{id}` : `GET` a single generic location
/locatios/{lid}/sub-locations/ : get generic sub-locations/
/location/{lid}/locations-on-path/ :get generic locations from the root to the given location



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
