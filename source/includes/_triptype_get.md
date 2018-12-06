## Get trip type object

This endpoint allows you to batch update availability information for a trip type. The request includes an array of trip start dates and times. By default, Arctic will make the necessary changes so that the trip calendar in Arctic matches the provided list of start dates and times, including creating trips, updating openings and canceling trips.

```php
<?php

require 'init.i.php';

$trip_type = \Arctic\Model\Trip\TripType::load(1);
```

```shell
curl "https://outfitter.arcticres.com/api/rest/triptype/1"
  -H "Authorization: Bearer token"
```

> The above request returns a trip type object.

### HTTP Request

`GET https://outfitter.arcticres.com/api/rest/triptype/<id>`

### URL Parameters

Parameter | Type | Default | Description
--------- | ---- | ------- | -----------
id | int | *required* | The ID of the trip type.

### Response Attributes

The response returns a [trip type object](#trip-type-object).

