---
swagger: "2.0"
x-collection-name: Square
x-complete: 1
info:
  title: Square Connect
  description: client-library-for-accessing-the-square-connect-apis
  termsOfService: https://connect.squareup.com/tos
  contact:
    name: Square Developer Platform
    url: https://squareup.com/developers
    email: developers@squareup.com
  version: "2.0"
host: connect.squareup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/{location_id}/cash-drawer-shifts:
    get:
      summary: Provides the details for all of a location's cash drawer shifts during
        a date range. The date range you specify cannot exceed 90 days.
      description: Provides the details for all of a location's cash drawer shifts
        during a date range. The date range you specify cannot exceed 90 days.
      operationId: ListCashDrawerShifts
      x-api-path-slug: v1location-idcashdrawershifts-get
      parameters:
      - in: query
        name: begin_time
        description: The beginning of the requested reporting period, in ISO 8601
          format
      - in: query
        name: end_time
        description: The beginning of the requested reporting period, in ISO 8601
          format
      - in: path
        name: location_id
        description: The ID of the location to list cash drawer shifts for
      - in: query
        name: order
        description: The order in which cash drawer shifts are listed in the response,
          based on their created_at field
      responses:
        200:
          description: OK
      tags:
      - Provides
      - Details
      - Of
      - Locations
      - Cash
      - Drawer
      - Shifts
      - During
      - Date
      - Range
      - ""
      - Date
      - Range
      - You
      - Specify
      - Cannot
      - Exceed
      - "90"
      - Days
---