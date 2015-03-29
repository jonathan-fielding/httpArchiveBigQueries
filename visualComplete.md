#Visual Complete

##Average
SELECT
SUM(visualComplete)/COUNT(visualComplete)
FROM [httparchive:runs.2015_03_01_pages]

##10th, 25th, 50th, 75th and 90th percentiles

SELECT
NTH(10, quantiles(visualComplete,100)) tenth,
NTH(25, quantiles(visualComplete,100)) twenty_fifth,
NTH(50, quantiles(visualComplete,100)) median,
  NTH(75, quantiles(visualComplete,100)) seventy_fifth,
  NTH(90, quantiles(visualComplete,100)) ninetieth
FROM [httparchive:runs.2015_03_01_pages]