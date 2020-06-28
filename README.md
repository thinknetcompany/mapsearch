# THiNKNET Maps

![THiNKNET Maps Logo](/static/image/logo_thinknet_maps.png)

**Thinknet Maps** สำหรับการใช้งานแผนที่ดิจิตอลด้วย Library ของ Mapbox-GL
ให้บริการข้อมูลบนแผนที่ซึ่งมี Map Style ไว้ให้เลือกใช้กว่า 10 แบบ

**Official Site** : [https://maps.thinknet.co.th](https://maps.thinknet.co.th)

**For Developers** : [https://developer-maps.thinknet.co.th](https://developer-maps.thinknet.co.th)
สำหรับจัดการ API Key และรับสิทธิ์การเข้าถึง THiNKNET Maps บน Application ของคุณ

**ดูตัวอย่างเพิ่มเติมได้ที่**: [DEMO](https://demo-maps.thinknet.co.th)

## :clipboard: Features

- [แสดงแผนที่บนเว็บไซต์](#get-started)
- [การกำหนดการแสดงภาษาบนแผนที่](./th/MAPSTYLE.md#การกำหนดการแสดงภาษาบนแผนที่)
- [Map Style](#map-style)
  - [เปลี่ยน Map Style](#change-map-style)
- [API Document](#)
  - [Search](./th/API_SEARCH.md)
  - [Suggest](./th/API_SUGGEST.md)
  - [Reverse Geocoding](./th/API_REVERSE_GEOCODING.md)
  - [Public Transport Routing](./th/API_PUBLIC_TRANSPORT_ROUTING.md)
  - [Static Data](./th/API_STATIC_DATA.md)

## :inbox_tray: ติดตั้ง mapbox-gl

### ติดตั้งผ่าน NPM

```shell
$ npm install mapbox-gl --save
```

จากนั้นนำ `mapbox-gl` เข้าสู่โปรเจค

```javascript
const mapboxgl = require('mapbox-gl')
require('node_modules/mapbox-gl/dist/mapbox-gl.css')
```

---

### หรือสำหรับใช้บน HTML

```html
<script src='https://api.tiles.mapbox.com/mapbox-gl-js/v1.3.2/mapbox-gl.js'></script>
<link href='https://api.tiles.mapbox.com/mapbox-gl-js/v1.3.2/mapbox-gl.css' rel='stylesheet' />
<script src="https://api-maps.thinknet.co.th/libs/thinknetmaps.1.0.0-plugin.min.js"></script>
```

## :electric_plug: เริ่มใช้งาน Maps API

<a name="get-started"></a>

### เริ่มต้นสร้างแผนที่

สร้าง div สำหรับเป็นพื้นที่ให้ render map ลงบนหน้าเว็บ และก่อนที่จะใช้คุณต้องทำการสร้าง `app_id` และ `api_key` จาก [THiNKNET Maps](https://developer-maps.thinknet.co.th)
เพื่อนำมาใช้งานกับแผนที่ของคุณ

```html
<html>
  <head>
    <script src='https://api.tiles.mapbox.com/mapbox-gl-js/v1.3.2/mapbox-gl.js'></script>
    <link href='https://api.tiles.mapbox.com/mapbox-gl-js/v1.3.2/mapbox-gl.css' rel='stylesheet' />
    <script src="https://api-maps.thinknet.co.th/libs/thinknetmaps.1.0.0-plugin.min.js"></script>
  </head>
  <body>
    <div id="map" style="height: 100vh;" />
    <script>
      mapboxgl.accessToken = '';
      var style_name = 'ivory';
      var app_id = '{YOUR_APP_ID}';
      var api_key = '{YOUR_API_KEY}';
      var lang = 'th';
      var style = 'https://api-maps.thinknet.co.th/v2/maps-styles/' + style_name + '?app_id=' + app_id + '&api_key=' + api_key + '&lang=' + lang;
      var map = new mapboxgl.Map({
        container: 'map', // id ของ div ที่จะให้ map ไป render
        style: style, // ที่อยู่ MapStyle ของ THiNKNET Maps
        center: [100.531326, 13.726854], // ค่าพิกัดเริ่มต้น [lng, lat]
        zoom: 10 // ค่า Zoom level เริ่มต้น
      });

      const TNMapsLogo = new THINKNETMapsLogo({ position: 'bottom-left' }) // position: bottom-left, top-left, top-right, bottom-right
      map.addControl(TNMapsLogo)
    </script>
  </body>
</html>
```

ชื่อของ container จะต้องตรงกับ ID ของ div ที่ใช้แสดงแผนที่ และคุณก็สามารถใช้ชื่อ container อื่นๆได้เช่นกัน

### THiNKNET Maps style parameter

| Name | Description | Default |
|------|-------------|---------|
| style_name | ชื่อของ Map Style | ivory |
| app_id | Application ID ของคุณ | - |
| api_key | API key ของคุณ | - |
| lang | ภาษาที่อยู่บนแผนที่ภายในประเทศไทย มี 3 แบบ [ th, en, th-en ] | th |

<a name="map-style"></a>

### Map Styles

#### รายชื่อ Map Style

- [almond](./th/MAPSTYLE.md#almond)
- [cha-thai](./th/MAPSTYLE.md#cha-thai)
- [charcoal](./th/MAPSTYLE.md#charcoal)
- [cloudy](./th/MAPSTYLE.md#cloudy)
- [hybrid](./th/MAPSTYLE.md#hybrid)
- [ivory](./th/MAPSTYLE.md#ivory)
- [lightsteel](./th/MAPSTYLE.md#lightsteel)
- [midnight](./th/MAPSTYLE.md#midnight)
- [satellite](./th/MAPSTYLE.md#satellite)
- [spearmint](./th/MAPSTYLE.md#spearmint)
- [terrain](./th/MAPSTYLE.md#terrain)

การใช้งาน feature ต่างๆ ของ mapbox-gl สามารถเข้าไปดูต่อได้ที่ [https://docs.mapbox.com/mapbox-gl-js/api/](https://docs.mapbox.com/mapbox-gl-js/api/)
