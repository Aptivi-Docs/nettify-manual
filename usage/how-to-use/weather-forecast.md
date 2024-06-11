---
description: We need to filter and build the VT sequences.
---

# ☀️ Weather Forecast

If you want to get weather forecast information in your city, you can use the `WeatherForecast` class from the `Nettify.Weather` namespace that contains:

* `GetWeatherInfo()`
* `ListAllCities()`

{% hint style="info" %}
There is an alternative version, called `WeatherForecastOwm`, that gets weather information from OpenWeatherMap. The normal `WeatherForecast` class gets info from [The Weather Channel](https://weather.com/).
{% endhint %}

These functions download the weather information for either the specified city ID or city name and return the relevant weather information, `WeatherForecastInfo`, that contains these properties:

* `WeatherCondition Weather`
* `UnitMeasurement TemperatureMeasurement` (see [weather conditions](https://openweathermap.org/weather-conditions))
* `double Temperature`
* `double Humidity`
* `double WindSpeed`
* `double WindDirection`

where the `UnitMeasurement` is:

* `Kelvin`
  * Measurement for `Temperature` and `FeelsLike` is `K` (Kelvin)
  * Measurement for `WindSpeed` is `m.s` (Meters per second)
  * Measurement for `Pressure` is `hPa` (Hectopascal)
* `Metric`
  * Measurement for `Temperature` and `FeelsLike` is `C` (Celsius)
  * Measurement for `WindSpeed` is `m.s` (Meters per second)
  * Measurement for `Pressure` is `hPa` (Hectopascal)
* `Imperial`
  * Measurement for `Temperature` and `FeelsLike` is `F` (Fahrenheit)
  * Measurement for `WindSpeed` is `mph` (Miles per hour)
  * Measurement for `Pressure` is `hPa` (Hectopascal)

{% hint style="warning" %}
`WeatherForecast` requires an API key that you can get from your IBM [Weather.com](https://www.ibm.com/products/environmental-intelligence-suite) dashboard. You'll need a package of **15 Day** weather forecast. **Kelvin is not supported in this mode.**

`WeatherForecastOwm` requires providing the OpenWeatherMap API key for each weather operation, which you can get by [visiting this page](https://home.openweathermap.org/api\_keys).
{% endhint %}

### Asynchronous Operation

For web development and other cases where asynchronous development is appropriate, you can use the functions that are suffixed with the `Async` suffix.
