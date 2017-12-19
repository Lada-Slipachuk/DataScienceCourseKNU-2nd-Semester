## Лабораторна робота 2
1.
```r
> list1 <-  list(observationA = c(1:5, 7:3), observationB = matrix(1:6, nrow=2))
> list1
$observationA
 [1] 1 2 3 4 5 7 6 5 4 3
$observationB
     [,1] [,2] [,3]
[1,]    1    3    5
[2,]    2    4    6

> lapply(list1, sum)
$observationA
[1] 40
$observationB
[1] 21
```
2.
```r
> lapply(list1, range)
$observationA
[1] 1 7
$observationB
[1] 1 6

> sapply(list1, range)
     observationA observationB
[1,]            1            1
[2,]            7            6
```
3.
```r
> lapply(split(InsectSprays, f=InsectSprays["spray"]), function(x) mean(x$count))
$A
[1] 14.5
$B
[1] 15.33333
$C
[1] 2.083333
$D
[1] 4.916667
$E
[1] 3.5
$F
[1] 16.66667
> 
```
