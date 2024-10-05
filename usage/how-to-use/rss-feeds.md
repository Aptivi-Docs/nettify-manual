---
description: News right at your fingertips!
icon: newspaper
---

# RSS Feeds

If you want to get all RSS feeds from a single site, you can use the `RSSTools` class from the `Nettify.Rss` namespace.

First, create a new instance of the `RSSFeed` class that contains the necessary constructor.

```csharp
public RSSFeed(string FeedUrl, RSSFeedType FeedType)
```

Then, call either `Refresh()` or `RefreshAsync()` to get the latest information about your feed, depending on the scenario. If you're either doing web development, or you're developing in an asynchronous program, call the `RefreshAsync()` function where appropriate.

The constructor provides the following required arguments:

* `FeedUrl`: specifies the URL to the RSS feed, for example, [https://www.techrepublic.com/rssfeeds/articles/](https://www.techrepublic.com/rssfeeds/articles/)
* `FeedType`: specifies the feed type to parse
  * `RSS2`: Assumes that the RSS feed in the given URL is an RSS 2 feed
  * `RSS1`: Assumes that the RSS feed in the given URL is an RSS 1 feed
  * `Atom`: Assumes that the RSS feed in the given URL is an Atom feed
  * `Infer`: Automatically detects the RSS feed type

For the RSS feed info, `RSSFeed` contains the following properties:

* `FeedUrl`: URL to the feed
* `FeedType`: Feed type as described above
* `FeedTitle`: Feed title provided by the host
* `FeedDescription`: Feed description provided by the host
* `FeedArticles`: List of feed articles

FeedArticles is a list of feed articles, `RSSArticle`, that you can enumerate within the for loop, for example:

```csharp
var feed = new RSSFeed("feedurl", RSSFeedType.Infer);
foreach (RSSArticle article in feed.FeedArticles)
{

}
```

This class contains the following properties:

* `ArticleTitle`: Title of the article
* `ArticleLink`: Link to the article
* `ArticleDescription`: Description or summary of the article
* `ArticleVariables`: Additional article parameters

## Searching RSS feeds

When it comes to searching RSS feeds, Nettify uses Feedly to give you a functionality that allows you to search Feedly for all the RSS feeds. For instance, if you're searching for Linux using this feature, it'll return all feeds that have to do with Linux. Check out Feedly's website if you don't know what it is yet:

{% embed url="https://feedly.com/" %}

You can use the following functions:

* `GetRssFeeds(string searchTerm)`
* `GetRssFeedsAsync(string searchTerm)`

Once you call one of these functions, you can use this array of `SearcherInstance` to get information about the resultant feeds. If you go further and get an RSS feed instance using this searcher instance (`GetFeedFromSearcher(SearcherInstance feed)` and `GetFeedFromSearcherAsync(SearcherInstance feed)`), you can get an instance of `RSSFeed` that you can use to get articles.
