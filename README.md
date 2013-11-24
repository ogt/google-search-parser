google-search-parser
====================

Parses  ads, results from the HTML of  google search page results into json.

--
This module takes as input the HTML from a google search results and return a json structure of the following form
```
query_string : "",
ads : [
    {
        Domain : '', // e.g. ebay.com or amazon.com  (the domain portion of the display url)
        Title : '', 
        Line1 : '', 
        Line2 : '',  // If just one line - split by ' - ' to produce line 1 and line 2
        DisplayURL : '',
        URL : '',
        IsTop3 : true,
        IsBottom : false,
        Extensions : {  // http://cl.ly/0h0f2Y1h0d0g
            Review : {
                Quote : '',
                Author : '',
                Url : '',
            },
            Social : {
                Count : 100
            }
            Ratings : {
                Count : 999,
                Rating : 8.3
            },
            SiteLinks : [
                {
                    Title : '',
                    Url : ''
                }
                ...
            ],
            HasCallExtension : True/False
            HasLocation : True/False
            HasMobileApp : True/False
            HasDeal : True/False
            HasSocial : True/False
            HasSiteLinks : True/False
            HasRatings : True/False
            HasReviews :True/False
         }   

    },
    ...
]
results : [
    {
        Domain : 
        Title
        URL
        Text
        Extensions : {
           PublishedBy : { // http://cl.ly/1D3J0F262o2E
               Photo :
               Who :
               Date :
               Followers :
           }
           Sitelinks : [   // http://cl.ly/3l0H1U390R0b
               {
                   Title
                   URL
                   Text
               }
               ..
               
           ]
        }
        
    }
    ...
]
```
