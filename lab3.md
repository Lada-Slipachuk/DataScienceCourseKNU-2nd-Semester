## Лабораторна робота 3
1.
```r
> Sys.setlocale(locale = "ukrainian")
[1] "LC_COLLATE=Ukrainian_Ukraine.1251;LC_CTYPE=Ukrainian_Ukraine.1251;LC_MONETARY=Ukrainian_Ukraine.1251;LC_NUMERIC=C;LC_TIME=Ukrainian_Ukraine.1251"

> fileURL <- "http://data.gov.ua/file/152588/download?token=Nk14ZhWf"
> download.file(fileURL, destfile = "data.xls", mode = "wb")
trying URL 'http://data.gov.ua/file/152588/download?token=Nk14ZhWf'
Content type 'application/vnd.ms-excel' length 324096 bytes (316 KB)
downloaded 316 KB
> data <- read.xlsx("data.xls", sheetIndex = 1, startRow=6, as.data.frame=TRUE, encoding = "UTF-8")
> head(data)
  X1 Інформація Про.надання.списків.для.нагородження. X42739 X01.12.1 надання..список..нагородження
1  2 Інформація                Про проблемні питання   42739  01-12/2             проблема, питання
2  3 Інформація                Про звернення громадян  42739  01-12/3          звернення, громадяни
3  4 Інформація                Про звернення громадян  42739  01-12/4          звернення, громадяни
4  5 Інформація                 Про тимчасовий розпис  42740  01-12/5             тимчасово, розпис
5  6 Інформація                    Список працівників  42740  01-11/6             список, працівник
6  7 Інформація                  Про роботу з кадрами  42740  01-12/7                 робота, кадри
  електронний Управління.капітального.будівництва.Сумської.ОДА
1 електронний Управління капітального будівництва Сумської ОДА
2    паперова Управління капітального будівництва Сумської ОДА
3    паперова Управління капітального будівництва Сумської ОДА
4 електронний Управління капітального будівництва Сумської ОДА
5    паперова Управління капітального будівництва Сумської ОДА
6 електронний Управління капітального будівництва Сумської ОДА
  Управління.капітального.будівництва.Сумської.ОДА.1 X42740 основна NA. NA..1 NA..2
1   Управління капітального будівництва Сумської ОДА  42740 основна  NA    NA    NA
2   Управління капітального будівництва Сумської ОДА  42740 основна  NA    NA    NA
3   Управління капітального будівництва Сумської ОДА  42740 основна  NA    NA    NA
4   Управління капітального будівництва Сумської ОДА  42741 фінанси  NA    NA    NA
5   Управління капітального будівництва Сумської ОДА  42741 основна  NA    NA    NA
6   Управління капітального будівництва Сумської ОДА  42741 основна  NA    NA    NA
```
2.
```r
> download.file("https://d396qusza40orc.cloudfront.net/getdata%2Fdata%2Fss06hid.csv", destfile = "data.csv")
trying URL 'https://d396qusza40orc.cloudfront.net/getdata%2Fdata%2Fss06hid.csv'
Content type 'text/csv' length 4246554 bytes (4.0 MB)
downloaded 4.0 MB
>  data <- read.csv("data.csv")
> values <- data$VAL
> a <- lapply(values, function(x) if (!is.na(x) && x==24) TRUE else NA)
> length(a[!is.na(a)])
[1] 53
```
3.
```r
> url <- "http://d396qusza40orc.cloudfront.net/getdata%2Fdata%2Frestaurants.xml"
> doc <- xmlTreeParse(url,useInternal=TRUE)
> rootNode <- xmlRoot(doc)
> length(xpathApply(rootNode, '//row/row/zipcode[text()="21231"]'))
[1] 127
