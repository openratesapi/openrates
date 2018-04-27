# OpenRates API

OpenRates is a free JSON API delivering reliable, accurate and up-to-date currency exchange rate data sourced directly from the [European Central Bank](https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html). Exchange rates are updated daily at around 4:00pm CET. 

## Using the API

### Latest Rates
Query the API for the latest available exchange rates.

```http
GET http://api.openrates.io/latest
```

### Historical Rates
Query the API for historical exchange rate data as of the year 1999.

```http
GET http://api.openrates.io/2010-10-12
```

### Base Currency
The default base currency is Euro. In order to change the base currency, simply append the **base** parameter and set it to your preferred 3-letter currency code.

```http
GET http://api.openrates.io/latest?base=USD
```

### Specify Currencies
You can also limit the API result to specific currencies. In order to do so, specify the **symbols** parameter and set it to your preferred list of comma-separated 3-letter currency codes.

```http
GET http://api.openrates.io/latest?symbols=USD,GBP
```

### JSONP
The OpenRates API also supports cross-domain JSONP requests. Simply add the **callback** parameter to your request and set it to your preferred function name.

```http
GET http://api.openrates.io/latest?callback=MY_CALLBACK
```

### HTTPS
All queries can also be made using HTTPS.

```http
GET https://api.openrates.io/latest
```

### Questions?
For questions please feel free to contact us at [contact@openrates.io](mailto:contact@openrates.io)
