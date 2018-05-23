---
title: How to use an R interface with Airtable API
author: Amy McDougall
type: post
date: 2018-05-24T11:49:40+00:00
spacious_page_layout:
  - default_layout
categories:
  - Data Science
  - R
tags:
  - r

---
# How to use an R interface with an Airtable API
-------------------------------------------------
Hi folks, so this blog is about how to use an R interface with an Airtable API. 
We are going to be using this interface and API to pick our winner for our [T-shirt draw](https://twitter.com/LockeData/status/997170312323055616). We will also be using the dplyr function `sample_n()`.
There are a couple of different R packages that you can use but I used [Darko Bergant's package](https://github.com/bergant/airtabler).You'll also need to use `devtools`.

Set up
--------
To install `devtools` all you need to do is `install.packages("devtools")`.

Now you need to install [Darko Bergant's package](https://github.com/bergant/airtabler).
`devtools::install_github("bergant/airtabler")`

Next you need to generate the airtable API key from your [Airtable account](https://airtable.com/account) page.

Library
-------
Now that you have `devtools` and [bergant/airtabler](https://github.com/bergant/airtabler) installed you need load them into the session to be used. First```library(airtabler)```, then ```library(dplyr)```.



Retrieve the data as a data.frame
-----------------------------------
To retrieve the data as a `data.frame` you'll need your [Airtable API key]((https://airtable.com/account).
```r 
Sys.setenv("AIRTABLE_API_KEY"="<Your API key") #example key************** ```
Then you need to add the base that you want to pull the data from. ```r 
airtable <- airtabler::airtable("<base key>", "<Tab/sheet name>") #base key can be found in the API docs```.
Now you need to select the data that you want to use ```r
airtable <- airtable$`<Tab/sheet name>`$select_all()```.

In your enviroment you should now see in data:
airtable x obs. of x variable. You can click to the right of that to open the table if you want. 

Using the dplyr function `sample_n()`
---------------------------------------
Finally we have all the data we need in a `data.frame` we can now use the dplyr function. We just want to pick one row to be our winner.
```r 
sample_n(airtable, 1) #1 is the number of rows we want```

This is our result.```id  Twitter handle I want a chance to win a t-shirt Name
17 re************* @amymcdougall96                              Yes Amy 
                createdTime
17 2018-05-18T13:38:58.000Z ```

*(Note i used myself here as the example)*

Other bits you can do
-----------------------
If you don't want to select some random data here are a few other things you can do.
If you type
```airtable$`<your tab/sheet>` ```
You can get a list of functions available for you to play with 
```$list_records
function (offset = NULL, recursive = TRUE, filter_by_formula = NULL) 
{
    list_records(air_options, table, offset, recursive, filter_by_formula)
}
environment: ***********

$retrieve_record
function (record_id) 
{
    retrieve_record(air_options, table, record_id)
}
environment: ***********

$create_record
function (fields) 
{
    create_record(air_options, table, fields)
}
environment: ***********

$update_record
function (record_id, fields, method = "PATCH") 
{
    update_record(air_options, table, record_id, fields, method = method)
}
environment: ***********

$delete_record
function (record_id) 
{
    delete_record(air_options, table, record_id)
}
environment: *********** ```