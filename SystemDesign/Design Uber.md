
**Funcitonal Requirements:**
- Find Near by drivers
- Rider can request a ride.
- Update driver location - (continous some interaval of time)
- Pickup Confirm / driver accpetance
- Trip Updates/ ETA
- End the Trip

**Non - Functional Requirements**
- Highly Available
- Highly Scalable
- Consistent (Eventual)

![[uber flow.png]]

**Services:**
**User Service:**
- Registration, authentication, also works like an orchestrator and interacts with internal services like Trip manager, Cab Finder etc.

**WebSocket Handler Service:**
- Keep persistent connection b/n driver and system And also Rider and System.

**Communication Service:** 
- All the update push notificaton will go through the this service.
- It also store connection information of riders and drivers in cache.
	-  it can response to qureries like which websocket handler hold the connection for Rider R1
- It also acts like an orchestrator with thrid party solutions for email, SMS or push notification

**Cab Finder**
 - this service is responsible for assingnig a driver to rider.
 - This service can take the decission of choosing the best match based the some rule, like rating, ETA etc.
 - This service can take help of other service while choosing the best match.

**Location Service**
- It will listen to driver's  location and perist the data.
- It will return top K drivers near the area.
- it will also acts like an orchestration for third party map solution, for real time ETA like google maps.

**Trip Service**
- It will keep all the trip information for users and drivers.
- It will support payment team for settlements.

![[Screenshot 2023-05-21 at 1.22.21 AM.png]]



**API's**
- `updateDriverLocation(driverID, oldlat, oldlong, newlat, newlong )`
- `findNearbyDrivers(riderID, lat, long)`
- `requestRide(riderID, lat, long, dropOfflat,dropOfflong, typeOfVehicle)`
- `showETA(driverID, eta)`
- `confirmPickup(driverID, riderID, timestamp)`
- `showTripUpdates(tripID, riderID, driverID, driverlat, driverlong, time_elapsed, time_remaining)`
- `endTrip(tripID, riderID, driverID ,time_elapsed, lat, long)`


**Location Storage**
**Hash**
- Even Grid
- GeoHash
- Cartesian tiers

**Tree**
- QuadTree
- Google S2
- RTree

**Touch Points:**
- Security - WAF
- Payments
- Analytics

Geo hash of google HeadQuater: 
1001 10110 01001 11011 11010 (base 32 in binary) ->  9q9hvu (base32)
