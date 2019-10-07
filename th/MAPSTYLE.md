
## การเลือกใช้ map style

ในการเลือกใช้ style ของ map ให้กำหนด parameter style ในตอนสร้าง URL ไปยัง MapStyle แล้วใส่ชื่อ style ที่ต้องการ

```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/{ชื่อ style}

```
## รายชื่อ Map Styles
- [almond](#almond)
- [cha-thai](#cha-thai)
- [charcoal](#charcoal)
- [cloudy](#cloudy)
- [hybrid](#hybrid)
- [ivory](#ivory)
- [lightsteel](#lightsteel)
- [midnight](#midnight)
- [satellite](#satellite)
- [spearmint](#spearmint)
- [terrain](#terrain)

## ตัวอย่าง Map Style

### almond
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/almond?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style almond](../static/image/map-style/almond.png)

### cha-thai
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/cha-thai?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style cha-thai](../static/image/map-style/cha-thai.png)

### charcoal
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/charcoal?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style charcoal](../static/image/map-style/charcoal.png)

### cloudy
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/cloudy?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style cloudy](../static/image/map-style/cloudy.png)

### hybrid
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/hybrid?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style hybrid](../static/image/map-style/hybrid.png)

### ivory
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/ivory?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style hybrid](../static/image/map-style/ivory.png)

### lightsteel
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/lightsteel?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style lightsteel](../static/image/map-style/lightsteel.png)

### midnight
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/midnight?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style midnight](../static/image/map-style/midnight.png)

### satellite
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/satellite?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style satellite](../static/image/map-style/satellite.png)

### spearmint
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/spearmint?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style spearmint](../static/image/map-style/spearmint.png)

### terrain
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/terrain?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>

```
![map style terrain](../static/image/map-style/terrain.png)

## การกำหนดการแสดงภาษาบนแผนที่

ในการกำหนดการแสดงภาษาบนแผนที่ ให้กำหนด parameter lang ในตอนสร้าง URL ไปยัง MapStyle แล้วใส่อักษรย่อ ภาษา ที่ต้องการ ซึ่งในตอนนี้ map style รองรับภาษา ไทย อังกฤษ และ ไทย-อังกฤษ

| ภาษา | key ที่ใช้ |
|------|---------|
|  ไทย (default)|  th |
| อังกฤษ |  en |
| ไทย-อังกฤษ |  th-en |

### ตัวอย่าง การเรียกใช้ภาษา ไทย-อังกฤษ
```javascript
https://api-maps.thinknet.co.th/v2/maps-styles/ivory?app_id=<YOUR_APP_ID>&api_key=<YOUR_API_KEY>&lang=th-en

```
### การแสดงผล

![map th-en](../static/image/map-style/th-en-map.png)
