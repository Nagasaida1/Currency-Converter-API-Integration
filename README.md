## Currency Converter API Integration

## Overview

This is a Spring Boot application that integrates with a public API to provide real-time currency conversion functionality. The application fetches exchange rates and allows users to convert an amount from one currency to another.

## Features

Fetch real-time exchange rates from a public API.

Convert an amount from one currency to another.

Proper error handling for invalid inputs and external API failures.

Unit tests using JUnit.

## Technologies Used

Java 17+

Spring Boot 3+

Spring Web (for RESTful API)

Spring Boot Test (for unit testing)

Maven (for dependency management)

Open Exchange Rates API (or any public currency API)

## Prerequisites

Ensure you have the following installed:

Java 17+

Maven 3+

An API Key from Exchange Rates API or Open Exchange Rates

## Setup & Installation

Clone the repository

git clone https://github.com/Nagasaida1/Currency-Converter-API-Integration.git
cd currency-converter

Configure API Key

Open src/main/resources/application.properties and add your API key:

exchange.api.url=https://api.exchangeratesapi.io/latest
exchange.api.key=your_api_key_here

Build the project

mvn clean install

Run the application

mvn spring-boot:run

## API Endpoints

1. Fetch Exchange Rates

GET /api/rates?base=USD

![image](https://github.com/user-attachments/assets/7907c62c-f79e-41b5-b8e8-e47bb9faf542)


Example Response:

{
  "base": "USD",
  "rates": {
    "EUR": 0.945,
    "INR": 82.5
  }
}

2. Convert Currency

POST /api/convert

Request Body:

{
  "from": "USD",
  "to": "EUR",
  "amount": 100
}

![image](https://github.com/user-attachments/assets/a800c627-2b0f-400a-92e3-8bc2b6ba77cb)


Example Response:

{
  "from": "USD",
  "to": "EUR",
  "amount": 100,
  "convertedAmount": 94.5
}

## Running Tests

To run unit tests:

mvn test

Error Handling

400 Bad Request: Invalid currency codes.

500 Internal Server Error: External API failure.

## License

This project is open-source and available under the MIT License.

## Contact

For questions, reach out via nagasaidavelpula1704email@example.com.

