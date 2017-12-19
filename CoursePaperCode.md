## Кількість кібератак на Україну
У 2016 році
```r
> Month_of_year_2016 <- c ("January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December")
> Total_amount_of_attacks_in_2016 <- c (682, 914, 1048, 603, 524, 737, 374, 346, 411, 305, 458, 98)
> Attacks_2016 <- data.frame(Month_of_year_2016, Total_amount_of_attacks_in_2016)
> Attacks_2016
   Month_of_year_2016 Total_amount_of_attacks_in_2016
1             January                             682
2            February                             914
3               March                            1048
4               April                             603
5                 May                             524
6                June                             737
7                July                             374
8              August                             346
9           September                             411
10            October                             305
11           November                             458
12           December                              98

> sum(Total_amount_of_attacks_in_2016)
[1] 6500
```
У 2016 році
```r
> Month_of_year_2017 <- c ("January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December")
> Total_amount_of_attacks_in_2017 <- c (28, 153, 261, 617, 1316, 12500, 347, 85, 37, 105, 63, 12)
> Attacks_2017 <- data.frame(Month_of_year_2017, Total_amount_of_attacks_in_2017)
> Attacks_2017
   Month_of_year_2017 Total_amount_of_attacks_in_2017
1             January                              28
2            February                             153
3               March                             261
4               April                             617
5                 May                            1316
6                June                           12500
7                July                             347
8              August                              85
9           September                              37
10            October                             105
11           November                              63
12           December                              12
> 
> sum(Total_amount_of_attacks_in_2017)
[1] 15524
```
