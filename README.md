# Using Google Search Console data to detect Content Decay

This notebook is aimed at easing the process of identifying content a decay, which is perfectly explained in [this post from Animalz](https://www.animalz.co/blog/content-refresh/).

For any given content, if you don't update it, you may face a situation where the traffic will decrease at some point. You can run an analysis using your GA account with your own process or with [Animalz' tool](https://www.animalz.co/blog/free-content-tool/) but at the end of the day and as SEO profesionnal, you need to know which keywords have contributed the most to the drop you are observing. 

That's why I build this notebook on top of the amazing https://github.com/joshcarty/google-searchconsole library, hence please follow its instructions to allow the notebook to access you GSC data. Ths process is simple: 
1. Go to the Google Developer Console
2. Create a project 
3. Activate the GSC Reporting API 
3. Create credentials for an OAuth client ID, choosing the Other Application type
4. Download the client-secret.json file

__The idea is to know on which queries you dropped between last month and the peak phase for any content. If you already know that, a part of the job is done and you will have then to look at the current SERP landscape, the competition etc... to undertand why you dropped and how to solve it.__


# Limits

Please note that the GSC Query report is not 100% accurate (see https://twitter.com/Errioxa/status/1258466210850758658) which explains why you may not see the same numbers in the top pages and the top query per page. This is a known limitation but this notebook assumes that even if the data we get at keyword-level are not 100% accurate, the relative importance is the same. 

# Output 

The notebook will output a table with the data 
