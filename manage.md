
## :rocket: Using ScrapeOps for Logging & Scrapy Managment

To get your data showing on ScrapeOps and control scrapyd on your servers the steps are:


### 1) Install the ScrapeOps extention
Install the scrapeOps extention for Scrapy using the command below.

`pip install git+https://github.com/ScrapeOps/scrapeops-scrapy-sdk`



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


### 3) Whitelist our server
If you want to run/stop/re-run/schedule any jobs using ScrapeOps this step is needed. 
If we cannot reach your server via port 80 & 443 the server will be listed as read only on the servers page.

The following steps should work to whitelist our IP on Linux/Unix based servers that have UFW firewall installed:

 - **Step 1: Log into your server via SSH.**

 - **Step 2: Allow incoming connections from 46.101.44.87**

   **`sudo ufw allow from 46.101.44.87 to any port 443,80 proto tcp`**

 - **Step 3: Allow outgoing connections to 46.101.44.87**

   **`sudo ufw allow out to 46.101.44.87 port 433,80`**

 - **Step 4: Check firewall rules are implemented**

   **`sudo ufw status`**


Once this is done you should be able to run/re-run/stop/schedule jobs for this server from our site.
    
