---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 0
info:
  title: Xignite Rates Draw Yield Curve
  description: Draw a yield curve for a rate family.
  version: 1.0.0
host: www.xignite.com
basePath: xRates.json/XigniteRates
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
  /GetYield:
    get:
      summary: Get Yield
      description: Returns Yield to maturity for a specific bond reported by the price
        source selected in the input. Request against this operation counts as one
        hit.
      operationId: GetYield
      x-api-path-slug: getyield-get
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
      - Yield
  /DrawYieldCurve:
    get:
      summary: Draw Yield Curve
      description: Draw a yield curve for a rate family.
      operationId: postDrawyieldcurve
      x-api-path-slug: drawyieldcurve-get
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
      - Draw
      - Yield
      - Curve
  /DrawYieldCurvePreset:
    get:
      summary: Draw Yield Curve Preset
      description: Draw a yield curve for a rate family.
      operationId: postDrawyieldcurvepreset
      x-api-path-slug: drawyieldcurvepreset-get
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
      - Draw
      - Yield
      - Curve
      - Preset
  /DrawYieldCurveCustom:
    get:
      summary: Draw Yield Curve Custom
      description: Draw a yield curve for a rate family.
      operationId: postDrawyieldcurvecustom
      x-api-path-slug: drawyieldcurvecustom-get
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
      - Draw
      - Yield
      - Curve
      - Custom
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