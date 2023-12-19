---
description: We need to filter and build the VT sequences.
---

# ☀ Weather Forecast

If you want to get weather forecast information in your city, you can use the `WeatherForecast` class from the `Nettify.Weather` namespace that contains:

* `GetWeatherInfo(long, string, UnitMeasurement)`
* `GetWeatherInfo(string, string, UnitMeasurement)`
* `ListAllCities()`

The first three functions download the weather information for either the specified city ID or city name and return the relevant weather information, `WeatherForecastInfo`, that contains these properties:

* `long CityID`
* `string CityName`
* `WeatherCondition Weather`
* `UnitMeasurement TemperatureMeasurement` (see [weather conditions](https://openweathermap.org/weather-conditions))
* `double Temperature`
* `double FeelsLike`
* `double Pressure`
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
You're required to provide the API key for each weather operation, which you can get by [visiting this page](https://home.openweathermap.org/api\_keys).
{% endhint %}

### Asynchronous Operation

For web development and other cases where asynchronous development is appropriate, you can use the below functions which are declared to be asynchronous:

```csharp
public static async Task<WeatherForecastInfo> GetWeatherInfoAsync(long CityID, string APIKey, UnitMeasurement Unit = UnitMeasurement.Metric)
public static async Task<WeatherForecastInfo> GetWeatherInfoAsync(string CityName, string APIKey, UnitMeasurement Unit = UnitMeasurement.Metric)
public static async Task<Dictionary<long, string>> ListAllCitiesAsync()
```
