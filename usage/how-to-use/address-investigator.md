---
description: What is the server address when I just know my mail address?
---

# 📧 Address Investigator

Using this function is very simple! Just use the `Nettify.MailAddress` namespace in any piece of code you want to use the function, as in: `using Nettify.MailAddress;`

Just use the `IspTools` class that contains:

* `GetIspConfig(string, bool)`

This function downloads the relevant information for the specified mail address from the ISP database and processes it before returning the client configuration. Mail clients can use this configuration to set up automatic mail server configuration detection akin to Mozilla Thunderbird.
