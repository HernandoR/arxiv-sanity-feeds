<div align="center">
	<img alt="Arxiv Sanity Feeds" src="images/logo.png" width="200" height="200" />
	<h1>🦔 Arxiv Sanity RSS Feeds</h1>
	<p>
		<b>Subscribe to the content published on <a href="http://www.arxiv-sanity.com">Arxiv Sanity</a>.</b>
	</p>
	<br>
	<br>
	<br>
</div>

![Build badge for Arxiv Sanity Feeds](https://github.com/dend/arxiv-sanity-feeds/actions/workflows/spawnfeed.yml/badge.svg)

All this tool does is scrape [Arxiv Sanity](http://www.arxiv-sanity.com), and produce consumable RSS feeds that can be used in your favorite RSS reader (such as Feedly or Outlook).

Feeds are updated daily.

## Feed Locations

### Home Page

```http
https://hedgehog.den.dev/feeds/home.xml
```
### Top Hyped Papers (Daily)

```http
https://hedgehog.den.dev/feeds/tophype-day.xml
```

### Discussed Papers

```http
https://hedgehog.den.dev/feeds/discussions.xml
```

### Most Recent Papers (Weekly)

```http
https://hedgehog.den.dev/feeds/toprecent-week.xml
```

## Building

1. Install [Python 3](https://www.python.org/) on your target operating system.
2. Create a virtual environment with `python3 -m venv .env`.
3. Install required packages with `pip install -r src/feedingress/requirements.txt`.
4. Set up the Azure Storage [connection string](https://docs.microsoft.com/azure/storage/common/storage-account-keys-manage?tabs=azure-portal) environment variable (`AZURE_STORAGE_CONNECTION_STRING`) to the connection string that you obtain from the [Azure Portal](https://portal.azure.com).
5. Run the application: `python -m feedingress`.

Once the application runs, it will upload the generated RSS feeds to the Azure Storage account of choice.