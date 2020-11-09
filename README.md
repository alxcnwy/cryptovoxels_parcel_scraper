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

### Top 5 parcels per neighbourhood
```
######################  Top 5 parcels in AREA 51  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   1253  1259    4144                  194                          1
1    592   595    3904                  219                          2
2   1175  1180    3435                  273                          3
3    607   610    3164                  317                          4
4   1341  1347    2954                  357                          5

######################  Top 5 parcels in AXIES  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2466  2476    8233                   41                          1
1   2554  2564    3962                  213                          2
2   2627  2637    2497                  470                          3
3   2678  2688    2237                  549                          4
4   1677  1685    2069                  616                          5

######################  Top 5 parcels in BABYLON  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2175  2183    7393                   58                          1
1   2045  2053    5496                  113                          2
2   1852  1860    3023                  349                          3
3   1902  1910    2954                  357                          4
4   2027  2035    2570                  442                          5

######################  Top 5 parcels in BERLIN ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3940  3950    2141                  580                          1
1   3955  3965    2030                  632                          2
2   4002  4012    1614                  872                          3
3   3937  3947    1493                  960                          4
4   3973  3983    1251                 1209                          5

######################  Top 5 parcels in CERES ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3160  3170    3606                  252                          1
1   3192  3202    3429                  274                          2
2   3161  3171    3321                  290                          3
3   3135  3145    2503                  469                          4
4   3110  3120    2136                  582                          5

######################  Top 5 parcels in DEEP SOUTH  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2401  2411    3508                  260                          1
1   2161  2169    3465                  267                          2
2   1664  1672    3115                  326                          3
3   2444  2454    2986                  355                          4
4   1415  1421    2771                  398                          5

######################  Top 5 parcels in DOOM  ######################
   index   id  visits  visits_rank_overall  visits_rank_neighbourhood
0    203  204    6741                   72                          1
1    793  797    6570                   79                          2
2    496  498    5717                  103                          3
3    198  199    5593                  110                          4
4    505  507    5175                  126                          5

######################  Top 5 parcels in ELECTRON ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3359  3369     639                 2300                          1
1   3373  3383     503                 2683                          2
2   3372  3382     494                 2706                          3
3   3357  3367     482                 2751                          4
4   3378  3388     457                 2850                          5

######################  Top 5 parcels in EURO ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3646  3656    1248                 1213                          1
1   3639  3649    1218                 1260                          2
2   3634  3644    1115                 1380                          3
3   3638  3648     945                 1640                          4
4   3650  3660     804                 1899                          5

######################  Top 5 parcels in FANTASY FIELDS  ######################
   index   id  visits  visits_rank_overall  visits_rank_neighbourhood
0    537  539    9265                   30                          1
1    692  696    5208                  123                          2
2    795  799    3753                  233                          3
3    721  725    3146                  325                          4
4    304  305    3113                  327                          5

######################  Top 5 parcels in FRANKFURT  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   1131  1136    9160                   32                          1
1   1272  1278    7934                   48                          2
2   1344  1350    7618                   50                          3
3    511   513    7123                   63                          4
4    604   607    7110                   64                          5

######################  Top 5 parcels in GANGNAM  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2506  2516   15092                    9                          1
1   2510  2520   15018                   10                          2
2   2440  2450   12444                   16                          3
3   2555  2565   12409                   17                          4
4   2580  2590   11076                   23                          5

######################  Top 5 parcels in HIRO  ######################
   index   id  visits  visits_rank_overall  visits_rank_neighbourhood
0    541  543    4705                  152                          1
1    208  209    4003                  212                          2
2    174  175    3821                  227                          3
3    191  192    3509                  259                          4
4    912  916    3362                  285                          5

######################  Top 5 parcels in JUNKYARD  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2057  2065    4130                  198                          1
1   1359  1365    4089                  204                          2
2   1506  1512    3417                  275                          3
3   1467  1473    2739                  404                          4
4   1399  1405    2625                  432                          5

######################  Top 5 parcels in KITTIES  ######################
   index   id  visits  visits_rank_overall  visits_rank_neighbourhood
0    761  765   13091                   12                          1
1    693  697   13001                   13                          2
2    835  839    9833                   28                          3
3    898  902    6710                   74                          4
4    812  816    5223                  122                          5

######################  Top 5 parcels in LE MARAIS  ######################
   index   id  visits  visits_rank_overall  visits_rank_neighbourhood
0    439  441   12079                   18                          1
1    324  325   10780                   26                          2
2    362  364    8425                   38                          3
3    261  262    7249                   60                          4
4    546  549    7224                   61                          5

######################  Top 5 parcels in LITTLE CERES ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3193  3203    2001                  644                          1

######################  Top 5 parcels in LITTLE TOKYO  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   1291  1297   13530                   11                          1
1   1336  1342    7572                   52                          2
2    851   855    3762                  231                          3
3    890   894    3689                  238                          4
4   1096  1101    3570                  257                          5

######################  Top 5 parcels in MAKERS  ######################
   index   id  visits  visits_rank_overall  visits_rank_neighbourhood
0    991  995    4923                  139                          1
1    356  358    4662                  156                          2
2    320  321    4202                  188                          3
3    270  271    3901                  220                          4
4    318  319    3372                  283                          5

######################  Top 5 parcels in MARS  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2865  2875    2459                  481                          1
1   2748  2758    2424                  490                          2
2   2830  2840    2001                  644                          3
3   2719  2729    1549                  927                          4
4   2842  2852    1544                  929                          5

######################  Top 5 parcels in MEMES  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2578  2588    3457                  269                          1
1   2619  2629    1934                  673                          2
2   2317  2325    1664                  839                          3
3   2526  2536    1622                  865                          4
4   1648  1656    1294                 1156                          5

######################  Top 5 parcels in MIDTOWN  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2640  2650    6465                   84                          1
1   2987  2997    5911                   96                          2
2   2542  2552    4886                  146                          3
3   2973  2983    4422                  172                          4
4   2955  2965    4287                  180                          5

######################  Top 5 parcels in MODVILLE  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2960  2970   12589                   15                          1
1   2936  2946   11720                   19                          2
2   2898  2908   10899                   24                          3
3   2924  2934    9451                   29                          4
4   2690  2700    5745                  102                          5

######################  Top 5 parcels in MOON  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   1152  1157   11590                   20                          1
1   1267  1273    8288                   39                          2
2   1098  1103    7327                   59                          3
3   2325  2333    6734                   73                          4
4   1395  1401    3283                  299                          5

######################  Top 5 parcels in MUSIC DISTRICT  ######################
   index   id  visits  visits_rank_overall  visits_rank_neighbourhood
0    130  131    4425                  171                          1
1    308  309    4091                  203                          2
2     83   84    3614                  250                          3
3    165  166    3485                  264                          4
4     53   54    3108                  329                          5

######################  Top 5 parcels in NEUTRON ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3558  3568    1621                  867                          1
1   3591  3601    1458                  993                          2
2   3593  3603    1365                 1084                          3
3   3546  3556    1295                 1154                          4
4   3545  3555    1286                 1165                          5

######################  Top 5 parcels in NORTH POLE  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2108  2116    5407                  117                          1
1   2265  2273    4093                  202                          2
2   1935  1943    2815                  389                          3
3   1810  1818    2475                  478                          4
4   1916  1924    2336                  518                          5

######################  Top 5 parcels in NORTH TERRACE  ######################
   index   id  visits  visits_rank_overall  visits_rank_neighbourhood
0    139  140   10825                   25                          1
1    181  182    9253                   31                          2
2    309  310    9049                   34                          3
3    500  502    8667                   37                          4
4     30   31    8091                   45                          5

######################  Top 5 parcels in OASIS  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2154  2162    4595                  160                          1
1   1798  1806    4455                  170                          2
2   1588  1596    4307                  178                          3
3   1727  1735    3318                  291                          4
4   1915  1923    2629                  430                          5

######################  Top 5 parcels in PROTON ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3496  3506    5641                  107                          1
1   3495  3505    4675                  154                          2
2   3497  3507    3733                  236                          3
3   3471  3481    2112                  597                          4
4   3460  3470    2066                  618                          5

######################  Top 5 parcels in PROXIMA ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3017  3027    4713                  151                          1
1   3102  3112    3147                  324                          2
2   3103  3113    3052                  342                          3
3   3099  3109    2767                  399                          4
4   3106  3116    2302                  528                          5

######################  Top 5 parcels in PUNKS  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2186  2194    7197                   62                          1
1   2298  2306    6512                   81                          2
2   1663  1671    5642                  106                          3
3   2490  2500    5022                  136                          4
4   2467  2477    4902                  142                          5

######################  Top 5 parcels in ROME  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2704  2714    5559                  112                          1
1   2782  2792    4034                  209                          2
2   2735  2745    3463                  268                          3
3   2302  2310    2565                  444                          4
4   2657  2667    2278                  537                          5

######################  Top 5 parcels in SCRIPTING  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   1156  1161   11578                   21                          1
1    838   842    4832                  149                          2
2    725   729    4205                  187                          3
3   1277  1283    3047                  344                          4
4    876   880    2937                  362                          5

######################  Top 5 parcels in SHENZHEN  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2642  2652    8673                   36                          1
1   2357  2367    6492                   82                          2
2   2669  2679    6346                   89                          3
3   2473  2483    5561                  111                          4
4   2757  2767    5255                  120                          5

######################  Top 5 parcels in TE ARO  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2595  2605    8025                   46                          1
1   2231  2239    5707                  104                          2
2   2528  2538    5603                  109                          3
3   2392  2402    5419                  116                          4
4   2461  2471    5197                  124                          5

######################  Top 5 parcels in THE BRONX ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3286  3296    6883                   69                          1
1   3285  3295    5927                   94                          2
2   3277  3287    3691                  237                          3
3   3278  3288    3398                  277                          4
4   3276  3286    3282                  300                          5

######################  Top 5 parcels in THE CENTER  ######################
   index  id  visits  visits_rank_overall  visits_rank_neighbourhood
0      0   1   66039                    1                          1
1      1   2   45086                    2                          2
2      3   4   30591                    3                          3
3      2   3   25316                    4                          4
4      6   7   19296                    5                          5

######################  Top 5 parcels in THE PLAYA  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   2849  2859    5127                  129                          1
1   2882  2892    4275                  183                          2
2   2919  2929    3148                  323                          3
3   2890  2900    2277                  538                          4
4   2790  2800    2150                  577                          5

######################  Top 5 parcels in TOKYO ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3725  3735    2861                  381                          1
1   3851  3861    2442                  484                          2
2   3739  3749    2421                  491                          3
3   3745  3755    2384                  505                          4
4   3733  3743    2377                  509                          5

######################  Top 5 parcels in TRINITY ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   3221  3231    1384                 1070                          1
1   3242  3252    1344                 1101                          2
2   3229  3239    1138                 1348                          3
3   3220  3230    1029                 1503                          4
4   3234  3244     879                 1747                          5

######################  Top 5 parcels in WEST END  ######################
   index    id  visits  visits_rank_overall  visits_rank_neighbourhood
0   1352  1358    4599                  159                          1
1   1374  1380    4055                  206                          2
2   1499  1505    4005                  211                          3
3   1890  1898    2798                  392                          4
4   1686  1694    2529                  463                          5

```

## Contact
Want more analysis, reach out to me on Twitter :)
> `https://twitter.com/alxcnwy`