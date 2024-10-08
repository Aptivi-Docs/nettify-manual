---
description: What is the server address when I just know my mail address?
icon: envelope
---

# Address Investigator

Using this function is very simple! Just use the `Nettify.MailAddress` namespace in any piece of code you want to use the function, as in: `using Nettify.MailAddress;`

Just use the `IspTools` class that contains:

* `GetIspConfig(string, bool)`

This function downloads the relevant information for the specified mail address from the ISP database and processes it before returning the client configuration. Mail clients can use this configuration to set up automatic mail server configuration detection akin to Mozilla Thunderbird.

{% hint style="info" %}
Autoconfiguration information is taken from Mozilla Thunderbird's [automatic configuration server](https://autoconfig.thunderbird.net/v1.1/), and a full list of mail providers is [here](https://github.com/Aptivi/Nettify/blob/main/Nettify/assets/IspInfo/isps.txt).
{% endhint %}
