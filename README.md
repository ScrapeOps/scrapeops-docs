# ScrapeOps Docs
The following is documentation on how to setup and use ScrapeOps with your Scrapy spiders. 

## :computer: Demo
[:link: ScrapeOps Dashboard Demo]()

## :star: Features

- **Scrapy Job Stats & Visualisation**
  - :chart_with_upwards_trend: Individual Job Progress Stats
  - :bar_chart: Compare Jobs versus Historical Jobs
  - :100: Job Stats Tracked
    - :white_check_mark: Pages Scraped & Missed
    - :white_check_mark: Items Parsed & Missed
    - :white_check_mark: Item Field Coverage
    - :white_check_mark: Runtimes
    - :white_check_mark: Response Status Codes
    - :white_check_mark: Success Rates & Average Latencies
    - :white_check_mark: Errors & Warnings
    - :white_check_mark: Bandwidth

- **Health Checks & Alerts**
  - :male_detective: Custom Spider & Job Health Checks 
  - :package: Out of the Box Alerts - Slack (More coming soon!)
  - :bookmark_tabs: Daily Scraping Reports

 - **ScrapyD Cluster Management**
    - :link: Integrate With ScrapyD Servers
    - :alarm_clock: Schedule Periodic Jobs
    - :100: All Scrapyd JSON API Supported
    - :closed_lock_with_key: Secure Your ScrapyD with BasicAuth, HTTPS or Whitelisted IPs
 - **Proxy Monitoring (Coming Soon)**
    - :chart_with_upwards_trend: Monitor Your Proxy Account Usage
    - :chart_with_downwards_trend: Track Your Proxy Providers Performance
    - :bar_chart: Compare Proxy Performance Verus Other Providers
  

## :rocket: Getting Started

To use ScrapeOps you first need to [create a free account]() and get your free **API_KEY**.

[![Create Free Account](https://global-uploads.webflow.com/5e3228ed49887d6904a307ff/5e82e926b74fcd359c210d4f_Create-your-quiz-button.png)](https://scrapeops.io/)

There are 2 way you can use ScrapeOps:

1. [ScrapeOps Logger Mode](#logger_mode)
2. [ScrapyD Manager Mode](#scrapyd_mode)



### <a name="logger_mode" href="https://github.com/ScrapeOps/scrapeops-docs/blob/main/logger-readme.md"></a> 1) Spider Logger Mode
In this mode the ScrapeOps SDK will log all your scraping stats and generate statistics, graphs and trigger alerts on the ScrapeOps dashboard. Getting setup is very easy, you just need to add 3 lines to your Scrapy projects `settings.py` file and the ScrapeOps SDK will take care of the rest. 



**Detailed Read:** [ScrapeOps SDK Installation Guide](https://github.com/ScrapeOps/scrapeops-docs/blob/main/scrapy/scrapy-sdk-setup.md)

### <a name="scrapyd_mode" href=""></a> 2) ScrapyD Manager Mode
In this mode, if you connect ScrapeOps with your ScrapyD server you will be able to schedule and manage your ScrapyD spiders via the ScrapeOps dashboard. 

:heavy_exclamation_mark: **Note:** To use the stats, graphs and alerts functionality of ScrapeOps, you need to install the ScrapeOps SDK in your Scrapy spiders.

**Read:** [ScrapeOps ScrapyD Integration Guide](https://github.com/ScrapeOps/scrapeops-docs/blob/main/manage-readme.md)</a>

 
