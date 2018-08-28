swagger: "2.0"
x-collection-name: Amadeus
x-complete: 1
info:
  title: Amadeus
  description: amadeus-api-is-a-toolkit-designed-for-travel-agencies-who-want-to-develop-their-own-travel-products-rather-than-using-offtheshelf-solutions--with-this-tool-you-can-build-your-very-own-customised-applications-that-link-in-a-stable-and-secure-dialogue-with-our-global-distribution-system-gds-
  contact:
    name: Amadeus Innovation and Research
    url: https://sandbox.amadeus.com
  version: 1.0.0
host: api.sandbox.amadeus.com
basePath: /v1.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /flights/low-fare-search:
    get:
      summary: Get Flights Low Fare Search
      description: "This is the low fare search engine Amadeus uses to retrieve the
        best price for flights, based on our latest Master Pricer Travel Board technology.
        This document describes how to make a low fare search and how to handle the
        returned messages.\n\nThe message is composed of multiple results for given
        request. A result is defined by a unique combination of price, tax, passenger
        type, fare type, cabin, and availability for each requested segment. \n\nA
        result is then composed of single or multiple itineraries. Each itinerary
        is composed of an outbound leg, and, if a return date was specified, an inbound
        leg. Each leg is composed of a list of one or more flights, that the traveller
        will be required to take in order to get from the origin airport to the destination
        airport."
      operationId: getFlightsLowFareSearch
      x-api-path-slug: flightslowfaresearch-get
      parameters:
      - in: query
        name: adults
        description: The number of adult (age 12 and over) passengers traveling on
          this flight
      - in: query
        name: arrive_by
        description: The datetime by which the outbound flight should arrive, based
          on local time at the destination airport
      - in: query
        name: children
        description: The number of child (younger than age 12 on date of departure)
          passengers traveling on this flight who will each have their own separate
          seat
      - in: query
        name: currency
        description: The preferred currency for the results
      - in: query
        name: departure_date
        description: The date on which the traveler will depart from the origin to
          go to the destination
      - in: query
        name: destination
        description: IATA code of the city to which the traveler is going
      - in: query
        name: exclude_airlines
        description: If specified, no results will include any flights where any of
          these airlines is the marketing carrier
      - in: query
        name: include_airlines
        description: If specified, all results will include at least one flight where
          one or more of these airlines is the marketing carrier
      - in: query
        name: infants
        description: The number of infant (younger than age 2 on date of departure)
          passengers traveling on this flight
      - in: query
        name: max_price
        description: Maximum price of trips to find in the result set, in USD (US
          dollars) unless some other currency code is specified
      - in: query
        name: nonstop
        description: Setting this to true will find only flights that do not require
          the passenger to change from one flight to another
      - in: query
        name: number_of_results
        description: The number of results to display
      - in: query
        name: origin
        description: City code from which the traveler will depart
      - in: query
        name: return_by
        description: The time by which the inbound flight should arrive, based on
          local time at the airport specified as the origin parameter
      - in: query
        name: return_date
        description: The date on which the traveler will depart from the destination
          to return to the origin
      - in: query
        name: travel_class
        description: Searches for results where the majority of the itinerary flight
          time should be in a the specified cabin class or higher
      responses:
        200:
          description: OK
      tags:
      - Airlines
      - Flights
      - Low
      - Fare
      - Search