
## :rocket: Getting Started Logging Your Scrapy Data

To get your data showing on our dashboards & graphs only takes 2 minutes!
The steps are: 

### 1) Install the ScrapeOps extention
Install the scrapeOps extention for Scrapy using the command below.

pip install git+https://github.com/ScrapeOps/scrapeops-scrapy-sdk



### 2) Add your API key & config details
In the settings.py file, you need to do the following steps:

- **Add in the ScrapeOps extension:**

`EXTENSIONS = {
        'scrapeops_scrapy.extension.ScrapeOpsMonitor': 500, 
    }`
    
    
    
- **Disable the default Scrapy retry downloader middleware & add in the ScrapeOps one:**

`DOWNLOADER_MIDDLEWARES = {
        'scrapeops_scrapy.middleware.retry.RetryMiddleware': 550,
        'scrapy.downloadermiddlewares.retry.RetryMiddleware': None,  
    }`
    
    
    
 - **Set your ScrapeOps API key so your logs can be linked to your account:**

`SCRAPEOPS_API_KEY = 'YOUR-SCRAPEOPS-API-KEY-HERE'`

You can see your api key on the settings page in ScrapeOps
    
