# ![LOGO](logo.png) Lyft **flow**ground Connector

## Description

A generated **flow**ground connector for the Lyft API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/lyft.com/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:42:49+03:00

## API Description

Drive your app to success with Lyft's API

## Authorization

Supported authorization schemes:
- OAuth2
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Cost estimates

> Estimate the cost of taking a Lyft between two points.

*Tags:* `Public`

#### Input Parameters
* `ride_type` - _optional_ - ID of a ride type
    Possible values: lyft, lyft_line, lyft_plus, lyft_premier, lyft_lux, lyft_luxsuv.
* `start_lat` - _required_ - Latitude of the starting location
* `start_lng` - _required_ - Longitude of the starting location
* `end_lat` - _optional_ - Latitude of the ending location
* `end_lng` - _optional_ - Longitude of the ending location

### Available drivers nearby

> The drivers endpoint returns a list of nearby drivers' lat and lng at a given location.

*Tags:* `Public`

#### Input Parameters
* `lat` - _required_ - Latitude of a location
* `lng` - _required_ - Longitude of a location

### Pickup ETAs

> The ETA endpoint lets you know how quickly a Lyft driver can come get you

*Tags:* `Public`

#### Input Parameters
* `lat` - _required_ - Latitude of a location
* `lng` - _required_ - Longitude of a location
* `destination_lat` - _optional_ - Latitude of destination location
* `destination_lng` - _optional_ - Longitude of destination location
* `ride_type` - _optional_ - ID of a ride type
    Possible values: lyft, lyft_line, lyft_plus, lyft_premier, lyft_lux, lyft_luxsuv.

### The user's general info

> The v1 of this endpoint returns the user's ID, v2 will return more general info about the user. We require authentication for this endpoint, so we extract the user ID from the access token.

*Tags:* `User`

### List rides

> Get a list of past & current rides for this passenger.

*Tags:* `User`

#### Input Parameters
* `start_time` - _required_ - Restrict to rides starting after this point in time. The earliest supported date is 2015-01-01T00:00:00+00:00

* `end_time` - _optional_ - Restrict to rides starting before this point in time. The earliest supported date is 2015-01-01T00:00:00+00:00

* `limit` - _optional_ - The maximum number of rides to return. The default limit is 10 if not specified. The maximum allowed value is 50, an integer greater that 50 will return at most 50 results.


### Request a Lyft

> Request a Lyft come pick you up at the given location.

*Tags:* `User`

### Get the ride detail of a given ride ID

> Get the status of a ride along with information about the driver, vehicle and price of a given ride ID

*Tags:* `User`

#### Input Parameters
* `id` - _required_ - The ID of the ride

### Cancel a ongoing requested ride

> Cancel a ongoing ride which was requested earlier by providing the ride id.

*Tags:* `User`

#### Input Parameters
* `id` - _required_ - The ID of the ride

### Update the destination of the ride

> Add or update the ride's destination. Note that the ride must still be active (not droppedOff or canceled), and that destinations on Lyft Line rides can not be changed.

*Tags:* `User`

#### Input Parameters
* `id` - _required_ - The ID of the ride

### Add the passenger's rating, feedback, and tip

> Add the passenger's 1 to 5 star rating of the ride, optional written feedback, and optional tip amount in minor units and currency. The ride must already be dropped off, and ratings must be given within 24 hours of drop off. For purposes of display, 5 is considered the default rating. When this endpoint is successfully called, payment processing will begin.

*Tags:* `User`

#### Input Parameters
* `id` - _required_ - The ID of the ride

### Get the receipt of the rides.

> Get the receipt information of a processed ride by providing the ride id. Receipts will only be available to view once the payment has been processed. In the case of canceled ride, cancellation penalty is included if applicable.

*Tags:* `User`

#### Input Parameters
* `id` - _required_ - The ID of the ride

### Types of rides

> The ride types endpoint returns information about what kinds of Lyft rides you can request at a given location.

*Tags:* `Public`

#### Input Parameters
* `lat` - _required_ - Latitude of a location
* `lng` - _required_ - Longitude of a location
* `ride_type` - _optional_ - ID of a ride type
    Possible values: lyft, lyft_line, lyft_plus, lyft_premier, lyft_lux, lyft_luxsuv.

### Preset Prime Time percentage

> Preset a Prime Time percentage in the region surrounding the specified location. This Prime Time percentage will be applied when requesting cost, or when requesting a ride in sandbox mode.

*Tags:* `Sandbox`

### Propagate ride through ride status

> Propagate a sandbox-ride through various ride status

*Tags:* `Sandbox`

#### Input Parameters
* `id` - _required_ - The ID of the ride

### Preset types of rides for sandbox

> The sandbox-ridetypes endpoint allows you to preset the ridetypes in the region surrounding the specified latitude and longitude to allow testing different scenarios

*Tags:* `Sandbox`

### Driver availability for processing ride request

> Set driver availability for the provided ride_type in the city/region surrounding the specified location

*Tags:* `Sandbox`

#### Input Parameters
* `ride_type` - _required_
    Possible values: lyft, lyft_line, lyft_plus, lyft_premier, lyft_lux, lyft_luxsuv.

## License

**flow**ground :- Telekom iPaaS / lyft-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
