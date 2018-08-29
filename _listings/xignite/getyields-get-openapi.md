---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 0
info:
  title: Xignite Bonds Get Yields
  description: Returns Yield to maturity for the list of bonds specified in the input,
    as reported by the price source selected in the input. Each Yields object returned
    counts as one hit.
  version: 1.0.0
host: bonds.xignite.com
basePath: xBonds.json/XigniteBonds
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetYields:
    get:
      summary: Get Yields
      description: Returns Yield to maturity for the list of bonds specified in the
        input, as reported by the price source selected in the input. Each Yields
        object returned counts as one hit.
      operationId: GetYields
      x-api-path-slug: getyields-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Yields
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---