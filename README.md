# How to use this tool:

Go to *cogcc website html* and enter your search terms and hit search. The results page is [cogcc.state.co.us/COGIS/LiveQuery.html] and is the key to scraping the COGCC. Save this page (Chrome, upper right hand corner drop down menu-> save page as) to whatever directory you would like on your local machine. This will save the html file that we use to access the different well pages. 

Next, set In[2](where it says "file:///wherever you saved livequery.html") to the path where you just saved the html file. Also at this time, figure out the directory where you would like to save the logs and enter it at In[3] (where it says creates path to.../well logs/%s). 

This version of the scraper targets directional data and the gamma ray logs for each well (lines X and X). Obviously you can change this to open any of the links on each well page, I was specifically interested in directional and gamma data so that's why those lines in block 3 are formatted that way. The comments on those two lines indixate which ones they are

After you have set your paths and determined which logs you would like, run all the script and it will download all logs for all the wells that were returned in your search. The file structure for the downloads creates a folder named by each well API, and those contain the log data. You can change the naming convention if you want, but I found API was easiest. 

# Additional info
Also, a side note on scraping ethics: don't slam their servers with a ton of requests or they might just ban your IP. There is a 10 second time delay built in to the code so this won't be an issue. Good luck, happy scraping, and maybe the COGCC will get an api sooner than later.
