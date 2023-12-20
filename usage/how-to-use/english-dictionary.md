---
description: Define "dictionary".
---

# 📘 English Dictionary

Using this feature is very simple! Just use the `Nettify.EnglishDictionary` namespace in any piece of code you want to use the feature, as in: `using Nettify.EnglishDictionary;`

Just use the `DictionaryManager` class that contains:

* `GetWordInfo(string)`
* `GetWordInfoAsync(string)`

You can then use the resulting array to iterate through possible words and get the values from them.

{% hint style="info" %}
If you're going to use this library on web projects or in situations that require you to use the asynchronous version, use the `GetWordInfoAsync`.
{% endhint %}
