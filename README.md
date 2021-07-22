# Finding Best Location to open Restaurents/Furnitures Stores in Patna

## Table of Content

1. [INTRODUCTION: BUSINESS PROBLEM](#INTRODUCTION)
2. [DATA DESCRIPTION](#DATA) 
3. [METHODOLOGY](#MET)
4. [ANALYSIS](#Anal)
5. [RESULT](#RES)
6. [CONCLUSION](#CON)
   
## INTRODUCTION: BUSINESS PROBLEM <a name="INTRODUCTION"></a>

Patna capital of Bihar state, northern India. Patna is a riverside city that extends along the south bank of the Ganges. Total population of Patna is more than 6.5 Million. It has total 40 neighborhood. My project aims to find the best location to open a Café, Chinese Restaurant, Furniture store, American Restaurants in the city of Patna, India.The major **Target Audience would be business owners and stake holders planning to start their business at a location in Patna.**  

The Foursquare API is used to access the venues in the neighborhoods. Since, it returns less venues in the neighborhoods, we would be analysing areas for which countable number of venues are obtained. Then they are clustered based on their venues using Data Science Techniques. Here the k-means clustering algorithm is used to achieve the task. The optimal number of clusters can be obtained using silhouette score metrics. Folium visualization library can be used to visualize the clusters superimposed on the map of Patna. These clusters can be analyzed to help small scale business owners select a suitable location for their need such as Café, Chinese Restaurant, Furniture store and American Restaurants.

## DATA DESCRIPTION <a name="DATA"></a>


Dataset containing Neighbourhoods of Patna, the dataset holds the names Neighbourhood in Patna extracted from Wikipedia. Here is a link. 
1. https://en.wikipedia.org/wiki/Category:Neighbourhoods_in_Patna.
2. https://foursquare.com/

A total of 75 venues data have been obtained from Foursquare.


## METHODOLOGY <a name="MET"></a>


Now, we have the neighborhoods data of Patna (41 neighborhoods). We also have the most popular venues in each neighborhood obtained using Foursquare API. A total of 75 venues have been obtained in the whole city and 35 unique categories.

We can perform one hot encoding on the obtained data set and use it find the 10 most common venue category in each neighborhood. Then clustering can be performed on the dataset. Here K Means clustering technique have been used. To find the optimal number of clusters silhouette score metric technique is used.

The clusters obtained can be analyzed to find the major type of venue categories in each cluster. This data can be used to suggest business people, suitable locations based on the category.

## ANALYSIS <a name="Anal"></a>


From the graph we can see that Buddha Colony and Serpentine Road returned the highest number of venues i.e. 21.

![](https://media-exp3.licdn.com/dms/image/C4D12AQGs-XtAmKbsww/article-inline_image-shrink_1000_1488/0/1625773437545?e=1632355200&v=beta&t=n3zBq67DFCm7Fr9V7r0fgskgFrRYICmgEz8eMbX5Smo)

There are many techniques are available in Data science field. For my project,  K-Nearest Neighbor (KNN) clustering algorithm is used. It is an unsupervised machine learning technique that clusters the given data into K number of clusters. For optimal result we need to select the best value for K. Here, the silhouette score is used to find the best value for K. 

![](https://media-exp3.licdn.com/dms/image/C4D12AQF-Cw7yUVmZhQ/article-inline_image-shrink_1000_1488/0/1625773704126?e=1632355200&v=beta&t=913jqfDdgYrH4ke0UnDH1OK7k0NB6tgmhfRW-0m_0BQ)

Now we have cleaned data and found all the prerequisite to model our data From the graph it looks cluster 4 could be the better one. so, let's use number of clusters as 4.

We can now use the cluster labels to show the city districts marked with a cluster-specific color on a map, again using folium: As you can see in the map every cluster had given different colors. so there are total 4 cluster of different color cluster 1 color is Purple, Cluster 2 color is sky blue, Cluster 3 color is red and cluster 4 color is Fade yellow.

![](https://media-exp3.licdn.com/dms/image/C4D12AQETjy4ORDGtsg/article-inline_image-shrink_1000_1488/0/1625774453222?e=1632355200&v=beta&t=k4kAeq3pXqT3TlRa6GF6I4RZITkVH5v5EyqmyI5NwYc)


## RESULT <a name="RES"></a>


We now can show four clusters with the most common venues


![](https://media-exp3.licdn.com/dms/image/C4D12AQEb_5oeOK3mCw/article-inline_image-shrink_1000_1488/0/1625775783419?e=1632355200&v=beta&t=GQisZcTpSWy3RlNYNycZl4b6_n-jeYGA3pY-E-SL-jU)

Above are the subplots of all cluster with top 5 common venues in it.

### 1. Best Location to open Chinese Restaurant
Kankarbagh , Boring Road, Frazer Road , Rajender nagar are the best neighborhoods for Chinese Restaurant as in Cluster 2 and Cluster 4 has no such Restaurant so if anyone wants to open Chinese Restaurant then the business be in profit.

### 2. Best Location to open Cafes
Bhita , Masaurhi have no Cafe to chill out so the people who live there would covered big distance if they want to go to Cafe. As those area are still not well developed so if new concept like cafe will start then there is a high probability to make good money

### 3. Best Location to open American Restaurant
People of Patna also like American style food like Fries , Burgers etc and also there is not so many american restaurant so if anyone wants to open American Restaurant then it will be a game changer for stakeholders. Places like Exhibition Road , New Karbhigya ,Gandhi maidan marg are well developed and good for business

### 4. Best Location to open Furniture store
After Food the most growing business in Patna is Furniture Stores. Places like Digha , Buddha Colony , Danapur are good to start.


## CONCLUSION <a name="CON"></a>


Purpose of this project was to analyze the neighborhoods of Patna and create a clustering model to suggest places to start a new business based on the category. The neighborhoods data was obtained from Wikipedia and the Foursquare API was used to find the major venues in each neighborhood.Then locations were used to create a clustering model. The best number of clusters i.e. 4 was obtained using the silhouette score. Each cluster was examined to find the most venue categories present, that defines the characteristics for that particular cluster.A map showing the clusters has been provided. Both of these can be used by stakeholders to decide the location for the required type of business.

## THANK YOU
I hope you found the project useful and interesting. This project was deveoped for the Applied Data Science Capstone as part of the IBM Data Science Professional Certificate provided through Coursera. Feel free to  download this project for your requirements and you can ask me also on -- [Shrey Bhardwaj](https://www.linkedin.com/in/shrey-bhardwaj-69076317b/).






