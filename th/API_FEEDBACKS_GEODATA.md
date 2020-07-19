## API Document

* [Reverse Geocoding v2](./API_REVERSE_GEOCODING_V2.md)

---

## Feedbacks Geo Data

การตอบกลับแก้ไขข้อมูล

* [ตัวอย่างการใช้งาน](#ตัวอย่างการใช้งาน0)

> **POST** `https://api-maps.thinknet.co.th/v1/feedbacks/geo`

### Data Fields
| Property | Description | Type | Request |
|----------|-------------|------|---------|
| lat | ค่าละติจูดของตำแหน่งที่ต้องการ | number | Yes |
| lng | ค่าลองจิจูดของตำแหน่งที่ต้องการ | number | Yes |
| poiname | ชื่อของสถานที่ (ถ้า) | string | - |
| street | ชื่อซอยหรือถนน | string | - |
| tambon | ชื่อตำบล | string | - |
| amphoe | ชื่ออำเภอ | string | - |
| province | ชื่องจังหวัด | string | - |
| postalcode | รหัสไปรษณีย์ | string | - |
| ref1 | ข้อมูลอ้างอิง 1 | string | - |
| ref2 | ข้อมูลอ้างอิง 2 | string | - |
| app_id | Application ID ที่ได้จากการ register | string | Yes |
| api_key | API Key ที่ได้จากการ register | string | Yes |

### ตัวอย่างการใช้งาน
##### Request

> URL : `https://api-maps.thinknet.co.th/v1/feedbacks/geo`
```
BODY :
{
    "lat": "13.7270270840907",
    "lng": "100.531414574661",
    "poiname": "บริษัท ทิงค์เน็ต จำกัด (สำนักงานใหญ่)",
    "street": "ถนนสีลม",
    "tambon": "สีลม",
    "amphoe": "บางรัก",
    "province": "กรุงเทพมหานคร",
    "postalcode": "10500",
    "ref1": "aaa",
    "ref2": "",
    "app_id": "${app_id}",
    "api_key": "${api_key}"
}
```

##### Response

```
{
    "code": 200,
    "message": "Sent Successfully"
}
```
