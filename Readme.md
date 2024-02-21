# ALIX Request


The request was to get all the dealerships for the brand Abarth. We were given this website as a strating point (from Hadia) : https://www.abarth.it/concessionari 

We initially thought of using the Google maps API or Scraping the webpage itself since it contains the important data. However ; 

1. Google maps API needs specific keywords to get the data. Some of the dealerships didn't contain any keyword that would let us find them using google maps API
2. Scraping it would take time, especially as we would need to use Celenium as it was not static. 

We inspected the network activity of the website when requesting dealerships in a certain area to better understand where it gets the data from, we noticed it uses a public api "https://dealerlocator.fiat.com/geocall/..." in which you can modify the coordinates X & Y and also specify the radius (maximum 100km). So we used that instead.

With that Public API, we can extract other brands from Fiat and also from any country we want. On top of that, it provides much more data than what Maps API or scraping would get us. (Legal codes, Emails, numbers, Fax code, ..)


