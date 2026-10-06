# SAFESEA Backend V1

## Run
Install Node.js 18+.

```bat
npm install
npm start
```

Open http://localhost:3000/api/health

## APIs
GET /api/health
GET /api/devices
POST /api/devices/heartbeat
POST /api/devices/location
GET /api/devices/:deviceId
POST /api/alerts
GET /api/alerts
POST /api/messages
GET /api/messages?deviceId=SS-0001

## Test heartbeat
```bat
curl -X POST http://localhost:3000/api/devices/heartbeat -H "Content-Type: application/json" -d "{\"deviceId\":\"SS-0001\",\"fishermanName\":\"Gowthaman\",\"boatName\":\"Sea Queen\",\"gpsStatus\":\"CONNECTED\",\"esp32Status\":\"CONNECTED\",\"alertStatus\":\"SAFE\",\"latitude\":11.0168,\"longitude\":76.9558,\"speed\":4.2}"
```

This V1 uses JSON files so it is easy to run. We can migrate to MySQL after the APK and website are communicating.
