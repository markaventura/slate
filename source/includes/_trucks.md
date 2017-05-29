# Trucks

## Create Truck

```shell
curl -X POST \
  http://localhost:3000/api/trucks \
  -H 'accesstoken: K3zSryrTsYsssgkbVawn5MmxzUoozxX6hUoTJ7Re9wE' \
  -F 'resource[plate_number]=ATA1234' \
  -F 'resource[official_receipt_number]=123456789' \
  -F 'resource[certificate_number]=987654321' \
  -F 'resource[make]=foo' \
  -F 'resource[model]=bar' \
  -F 'resource[rfid_id]=foobar' \
  -F 'resource[supplier_id]=1'
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "plate_number": "ATA1234",
  "official_receipt_number": "123456789",
  "certificate_number": "987654321",
  "make": "foo",
  "model": "bar",
  "is_deleted": false,
  "created_at": "2017-05-29T18:30:12.396Z",
  "updated_at": "2017-05-29T18:30:12.396Z",
  "supplier_id": 1,
  "status": "active",
  "rfid_id": 0
}
```

This endpoint creates new session.

### HTTP Request

`GET http://pngtrucking.com/api/trucks`

### Query Parameters

Parameter | Description
--------- | -----------
plate_number | The plat number of the truck.
official_receipt_number | The official receipt number of the truck.
certificate_number | The certificate number of the truck.
make | The make of the truck.
model | The current model of the truck.
rfid_id | The RFID number of the truck.
supplier_id | The supplier ID of the truck.

