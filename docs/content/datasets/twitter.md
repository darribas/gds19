#### Geo-referenced tweets

This dataset, provided as a shapefile, contains a collection of locations and
time stamps relating to [Twitter](http://twitter.com) postings within the 
municipality of Liverpool. The data was originally provided by Guy Lansley
from UCL and processed by Dani Arribas-Bel.

Every row in the dataset contains an individual tweet, and is provided with the
following information:

* `LAT`: latitude of the location where the posting took place.
* `LON`: longitude of the location where the posting took place.
* `YEAR`: year of posting.
* `MONTH`: month of posting.
* `DAY`: day of the month (1-31) when the message was posted.
* `DOW`: day of the week (0-6) when the message was posted.
* `HOUR`: hour of the posting.
* `MINUTE`: minute of the posting.
* `X`: longitude projected to the British National Grid ([EPSG:
  27700](http://epsg.io/27700)).
* `Y`: latitude projected to the British National Grid ([EPSG:
  27700](http://epsg.io/27700)).
* `LSOA11CD`: unique identifier code of the LSOA where the tweet location falls
  into.

**Source**: [Twitter](http://twitter.com) via Guy Lansley (UCL).

**Instructions**: given the Twitter license that applies to the data, this
dataset cannot be redistributed publicly online. For that reason, it has been
uploaded to the VITAL page of the course. You can find it instructions on
access and download on VITAL:

> VITAL ENVS3/563 --> Learning Resources --> Twitter dataset

The shapefile is provided as a compressed `.zip` file. Download it and extract
it where you can access and set the path appropriately.

