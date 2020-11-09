# Cryptovoxels Scraper & Analysis

This repo contains 2 python Jupyter notebooks:

1. `scrape_cryptovoxels.ipynb` for downloading cryptovoxels.com parcel data

2. `analysis.ipynb` for compiling, parsing and analyzing the scraped parcel data

## Scraper
Downloads parcel data for cryptovoxel plots.

For example, here is the data for my plot ("alex's bunker") as at 2020/11/08:
> https://www.cryptovoxels.com/parcels/1041

```
{
   "id":1041,
   "description":"the truth is out there",
   "address":"8 Stoll Freeway\nArea 51\nOrigin City",
   "neighbourhood":"Area 51 ",
   "visits":1094,
   "location":"178W,265N,",
   "size":"23\u00d716 metres",
   "area":368,
   "build_height":6,
   "elevation":"0 to 6 meters",
   "volume":17664
}
```

First download the data using "scrape_cryptovoxels.ipynb" then 

## Analysis


Questions answered include:

* how many plots are there per neighbourhood?
* what are the most popular neighbourhoods ranked on visits?
* what are the most popular streets ranked on visits?
* which neighbourhood has the largest parcels on average?
* which neighbourhood has the highest build heights on average?
* how do visits relate to parcel area?
* how do visits relate to the order in which parcels were minted?
* what are the top 5 plots in each neighbourhood ranked on visits?
* what are the top 5 most popular streets per neighbourhood?

See `analysis.ipynb` for full analysis - some findings below:

![1](https://imgur.com/qwJixpw.png)

![2](https://imgur.com/X41rVHx.png)

![3](https://imgur.com/VWbooPQ.png)

![4](https://imgur.com/3wJgjkg.png)

![5](https://imgur.com/CfE1HWg.png)

![6](https://imgur.com/eVYkI5E.png)

![7](https://imgur.com/PNicCgt.png)

## Contact
Want more analysis, reach out to me on Twitter :)
> `https://twitter.com/alxcnwy`