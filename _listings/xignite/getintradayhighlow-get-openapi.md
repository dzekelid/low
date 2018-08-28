---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 0
info:
  title: Xignite Currencies Get Intraday High Low
  description: Returns the high and the low ticks for today.
  version: 1.0.0
host: www.xignite.com/xCurrencies.json
basePath: /XigniteCurrencies
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetDailyOpenHighLowClosePrice:
    get:
      summary: Get Daily Open High Low Close Price
      description: Returns daily Open, High, Low, Close (OHLC) prices for a specific
        bond reported by the price source selected in the input. Daily OHLC data is
        provided for the most recent date for which data is provided by the price
        source. Request against this operation counts as one hit.
      operationId: GetDailyOpenHighLowClosePrice
      x-api-path-slug: getdailyopenhighlowcloseprice-get
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
      - Daily
      - Open
      - High
      - Low
      - Close
      - Price
  /GetYearlyHighLowPrice:
    get:
      summary: Get Yearly High Low Price
      description: Returns yearly high, low prices for a specific bond reported by
        the price source selected in the input. Request against this operation counts
        as one hit.
      operationId: GetYearlyHighLowPrice
      x-api-path-slug: getyearlyhighlowprice-get
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
      - Yearly
      - High
      - Low
      - Price
  /GetDailyOpenHighLowClosePrices:
    get:
      summary: Get Daily Open High Low Close Prices
      description: Returns daily Open, High, Low, Close (OHLC) prices for the list
        of bonds specified in the input. Daily OHLC data is provided for the most
        recent date for which data is provided by the price source. Each DailyOpenHighLowClosePrice
        object  returned counts as one hit.
      operationId: GetDailyOpenHighLowClosePrices
      x-api-path-slug: getdailyopenhighlowcloseprices-get
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
      - Daily
      - Open
      - High
      - Low
      - Close
      - Prices
  /GetYearlyHighLowPrices:
    get:
      summary: Get Yearly High Low Prices
      description: Returns yearly high, low prices for the list of bonds specified
        in the input, as reported by the price source selected in the input. Each
        YearlyHighLowPrice object returned counts as one hit.
      operationId: GetYearlyHighLowPrices
      x-api-path-slug: getyearlyhighlowprices-get
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
      - Yearly
      - High
      - Low
      - Prices
  /GetHistoricalHighLow:
    get:
      summary: Get Historical High Low
      description: Returns the high and the low ticks for a historical time range.
      operationId: postGethistoricalhighlow
      x-api-path-slug: gethistoricalhighlow-get
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
      - Historical
      - High
      - Low
  /GetIntradayHighLow:
    get:
      summary: Get Intraday High Low
      description: Returns the high and the low ticks for today.
      operationId: postGetintradayhighlow
      x-api-path-slug: getintradayhighlow-get
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
      - Intraday
      - High
      - Low
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