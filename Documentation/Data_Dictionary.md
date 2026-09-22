# SkyHigh Airlines – Data Dictionary

## Project Overview

This document describes the datasets used in the SkyHigh Airlines Power BI
dashboard project.

The project uses four datasets:

1. Airline Flights
2. Airline Passengers
3. Airline Revenue
4. Airline Airports

These datasets are used to analyze flight operations, delays, passenger
satisfaction, revenue performance and airport performance.

---

# 1. Airline Flights

**File:** `Airline_Flights.csv`

**Records:** 3,000

This dataset contains flight-level information including airline,
route, schedule, flight status, delays and aircraft type.

| Column | Data Type | Description |
|---|---|---|
| Flight ID | Text | Unique identifier for each flight |
| Airline | Text | Name of the airline |
| Source | Text | Departure airport code |
| Destination | Text | Arrival airport code |
| Departure Time | Date/Time | Scheduled/recorded departure date and time |
| Arrival Time | Date/Time | Scheduled/recorded arrival date and time |
| Status | Text | Flight status such as On-time |
| Delay (min) | Integer | Flight delay duration in minutes |
| Aircraft Type | Text | Type/model of aircraft used |
| Date | Date | Flight date |

---

# 2. Airline Passengers

**File:** `Airline_Passengers.csv`

**Records:** 3,000

This dataset contains passenger-level information including ticket class,
demographics, feedback score, baggage information and frequent flyer status.

| Column | Data Type | Description |
|---|---|---|
| Passenger ID | Text | Unique identifier for each passenger |
| Flight ID | Text | Identifier of the associated flight |
| Ticket Class | Text | Passenger ticket class |
| Age | Integer | Age of the passenger |
| Gender | Text | Gender of the passenger |
| Feedback Score | Integer | Passenger feedback/satisfaction score |
| Check-in Luggage | Text | Indicates whether the passenger checked in luggage |
| Frequent Flyer | Text | Indicates whether the passenger is a frequent flyer |

---

# 3. Airline Revenue

**File:** `Airline_Revenue.csv`

**Records:** 3,000

This dataset contains flight-level revenue information including ticket
price, total revenue, baggage fees and additional extras.

| Column | Data Type | Description |
|---|---|---|
| Flight ID | Text | Identifier of the associated flight |
| Ticket Price | Integer | Ticket price for the flight/passenger record |
| Total Revenue | Integer | Total revenue generated |
| Baggage Fee | Integer | Revenue generated from baggage fees |
| Extras | Integer | Revenue generated from additional extras |

---

# 4. Airline Airports

**File:** `Airline_Airports.csv`

**Records:** 10

This dataset contains airport information including location,
region and on-time performance.

| Column | Data Type | Description |
|---|---|---|
| Airport Code | Text | Unique airport code |
| City | Text | City where the airport is located |
| Country | Text | Country where the airport is located |
| Region | Text | Geographic region of the airport |
| On-Time % | Decimal | Airport on-time performance percentage |

---

# Relationships Between Datasets

The datasets can be connected using common identifiers.

### Flight Relationship

`Airline_Flights[Flight ID]`

connects with:

`Airline_Passengers[Flight ID]`

and:

`Airline_Revenue[Flight ID]`

### Airport Relationships

Airport codes from:

`Airline_Airports[Airport Code]`

can be associated with:

`Airline_Flights[Source]`

and:

`Airline_Flights[Destination]`

---

# Main Analysis Areas

The datasets support the following analysis areas:

## Flight Operations

- Total number of flights
- Flight status
- Average delay
- Delay by route
- Delay trends
- Aircraft type usage
- Delayed airports

## Revenue Analysis

- Total revenue
- Ticket price
- Baggage fee revenue
- Additional extras
- Revenue trends

## Passenger Analysis

- Passenger count
- Passenger demographics
- Ticket class
- Feedback score
- Frequent flyer analysis
- Passenger satisfaction

## Airport Analysis

- Airport location
- Region
- On-time performance

---

# Power BI Usage

The datasets are used in Power BI for:

- Data cleaning and transformation using Power Query
- Data modeling
- DAX calculations
- KPI development
- Interactive visualizations
- Flight operations analysis
- Revenue analysis
- Passenger insights
- Airport performance analysis
