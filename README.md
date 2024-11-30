# RemoCell/CellsData

NOT usable yet. For now subscribe to
[CellsData/issues/1](https://github.com/RemoCell/CellsData/issues/1).

## PERMANENT SCOPE

- Most of the following is non-negotiable because of the following somewhat opposing realities
  - the large size of the data, and
  - need to serve (and hence index and organize) data by rectangular geographic areas, and
  - GitHub limitations on background processing (scheduled GitHub Actions, like "cron"), and
  - intent to keep the simultaneous number of GitHub "releases" (potentially large files with
    unlimited downloads) down, so that
    - they are manageable (both automated and manual, if need be), and
    - the number of parallel downloads (by a user) is realistic (not too high as to allow the
      browser or app and client processing run without blocking other use), and
    - not approaching an (unpublished) limit on number of GitHub releases.
- When downloading, no data selection/filtering by country, primary (physical) operator or by
  virtual operator.
  - [Emergency cellular numbers](https://en.wikipedia.org/wiki/List_of_emergency_telephone_numbers)
    (such as 911 in the USA, Canada and many countries in Central and South America; 112 in most
    European and Asian countries) work regardless of the operator or SIM card (and without a SIM
    card, too).
  - If you happen to be near a country border, your emergency call may be handled by that other
    civilized country. While they can't arrange activities in your country, they could hopefully at
    least alert your country's emergency services.
  - [OpenCellID download](https://opencellid.org/downloads.php) does filter the data by country and
    MCC, but
    - it would complicate the background processing
    - it would increase number of files in storage, by orders of magnitude (because we still want
      geographical indexing/slicing for faster downloads).
    - Yes, by including cells of all operators (in the area) together the downloads are bigger, but
      they are more useful in case of emergency.
    - Yes, we could split the server data by country, or by country and primary (physical) operator.
      But, that would increase the number of storage files. Even though the files themselves would
      be smaller, the number of storage files (and hence, GitHub "releases") would increase. That
      would slow down background processing and it could approach an (unpublished) GitHub limit on
      number of releases.
    - TODO: primary operators: maintain a list of their MCC MNC tuples
    - Filtering *might* by possible on client side after the download.
- When downloading, the download size doesn't increase/decrease smoothly, but in (possibly uneven)
  steps.
- It's difficult to predict a download size. It's especially difficult to predict a download time,
  because the number of data files depends on both dimensions (width and height) of the selected
  area, and it varies.
- Incremental updates are difficult, limited, or not possible/feasible at all.

## LONG TERM OR PERMANENT SCOPE

- No data selection/filtering by virtual operator. Many countries don't have them listed, for
  example in [Wikipedia's list of operators of the Americas >
  Canada](https://en.wikipedia.org/wiki/List_of_mobile_network_operators_of_the_Americas#Canada));
  and [Wikipedia's list of virtual operators in the
  USA](https://en.wikipedia.org/wiki/List_of_mobile_virtual_network_operators_in_the_United_States)
  doesn't contain MCC MNC tuples.

 ## LICENSE and ATTRIBUTION
 
 Based on [OpenCelliD data](https://opencellid.org/downloads.php) and and from
[Wikipedia](https://en.wikipedia.org) ([Mobile country
code](https://en.wikipedia.org/wiki/Mobile_country_code) and related Wikipedia pages).

 ![Creative Commons Attribution-ShareAlike](https://opencellid.org/images/ccbysa_4.0_80x15.png)
 [OpenCelliD Project](https://opencellid.org/) is licensed under a [Creative Commons
 Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

Data and text on Wikipedia is available under the [Creative Commons Attribution-ShareAlike 4.0
License](https://en.wikipedia.org/wiki/Wikipedia:Text_of_the_Creative_Commons_Attribution-ShareAlike_4.0_International_License).
