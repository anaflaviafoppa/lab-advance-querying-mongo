![Ironhack Logo](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Answers

### 1. All the companies whose name match 'Babelgum'. Retrieve only their `name` field.
<!-- Your Code Goes Here -->

{
  filter:{"name":{"$eq":"Babelgum"}}
  sort: 
  limit: 
}

{
  _id: 52cdef7c4bab8bd675297da0
  name:"Babelgum"
  permalink:"babelgum"
}




### 2. All the companies that have more than 5000 employees. Limit the search to 20 companies and sort them by **number of employees**.

<!-- Your Code Goes Here -->
{
  filter:{"number_of_employees":{"$gt":5000}}
  sort: {"number_of_employees": 1}
  limit: 20
}



### 3. All the companies founded between 2000 and 2005, both years included. Retrieve only the `name` and `founded_year` fields.

<!-- Your Code Goes Here -->
{
  filter:{"$and":[{"founded_year": {"$gte":2000}},{"founded_year":{"$lte":2005}}]}
  sort: {"name":1}
  limit: 
}

{
  _id:52cdef7f4bab8bd67529c5b0
  name:10East
  founded_year:2002
}

{
  _id:52cdef7d4bab8bd675298e7e
  name: 1915 Studios
  founded_year:2004
}


### 4. All the companies that had a Valuation Amount of more than 100.000.000, and have been founded before 2010. Retrieve only the `name` and `ipo` fields.

<!-- Your Code Goes Here -->
{
  filter:{"$and":[{"ipo.valuation_amount":{"$gte":100000000}},{"founded_year":{"$lte":2010}}]}
  sort: {"name":1}
  limit: 
}

{
  _id:52cdef7c4bab8bd675297e7a
  name:"Amazon"
  founded_year:1994
founded_month
:
null
founded_day
:
null
deadpooled_year
:
null
deadpooled_month
:
null
deadpooled_day
:
null
deadpooled_url
:
null
tag_list
:
"virtualstorage, onlineshopping, virtualserver, crowdsource, grocery"
alias_list
:
""
email_address
:
""
phone_number
:
"(206) 266-1000"
description
:
""
created_at
:
"Tue Jul 31 06:46:49 UTC 2007"
updated_at
:
"Wed Oct 30 17:13:43 UTC 2013"
overview
:
"<p>Amazon.com, Inc. (AMZN), is a leading global Internet company and o..."
_id
:
52cdef7c4bab8bd67529859a
name
:
"BMC Software"
permalink
:
"bmc-software"
crunchbase_url
:
"http://www.crunchbase.com/company/bmc-software"
homepage_url
:
"http://www.bmc.com"
blog_url
:
"http://www.bmc.com/devops"
blog_feed_url
:
""
twitter_username
:
"bmcsoftware"
category_code
:
"software"
number_of_employees
:
null
founded_year
:
1980
founded_month
:
9
founded_day
:
19
deadpooled_year
:
null
deadpooled_month
:
null
deadpooled_day
:
null
deadpooled_url
:
null
tag_list
:
""
alias_list
:
""
email_address
:
"info@bmc.com"
phone_number
:
"800-841-2031"
description
:
""
created_at
:
"Tue Mar 18 14:04:07 UTC 2008"
updated_at
:
"Mon Oct 21 18:08:28 UTC 2013"
overview
:
"<p>Business Runs on IT. IT Runs on BMC Software.
Business runs better ..."
_id
:
52cdef7c4bab8bd675298760
name
:
"Baidu"
permalink
:
"baidu"
crunchbase_url
:
"http://www.crunchbase.com/company/baidu"
homepage_url
:
"http://www.baidu.com"
blog_url
:
""
blog_feed_url
:
""
twitter_username
:
"baidu_"
category_code
:
"search"
number_of_employees
:
6000
founded_year
:
1999
founded_month
:
10
founded_day
:
11
deadpooled_year
:
null
deadpooled_month
:
null
deadpooled_day
:
null
deadpooled_url
:
null
tag_list
:
"search"
alias_list
:
""
email_address
:
"ir@baidu.com"
phone_number
:
"86 10 8262 1188"
description
:
""
created_at
:
"Mon Apr 07 23:06:27 UTC 2008"
updated_at
:
"Mon Jan 06 10:56:31 UTC 2014"
overview
:
"<p>It is the largest Chinese website and Chinese search engine in the ..."

}

### 5. All the companies that have less than 1000 employees and have been founded before 2005. Order them by the number of employees and limit the search to 10 companies.

<!-- Your Code Goes Here -->

### 6. All the companies that don't include the `partners` field.

<!-- Your Code Goes Here -->

### 7. All the companies that have a null value on the `category_code` field.

<!-- Your Code Goes Here -->

### 8. All the companies that have at least 100 employees but less than 1000. Retrieve only the `name` and `number of employees` fields.

<!-- Your Code Goes Here -->

### 9. All the companies ordered by their IPO price in a descending manner.

<!-- Your Code Goes Here -->

### 10. The 10 companies with the highest amount of employees, order by the `number of employees`.

<!-- Your Code Goes Here -->

### 11. All the companies founded on the second semester of the year. Limit your search to 1000 companies.

<!-- Your Code Goes Here -->

### 12. All the companies founded before 2000 that have an acquisition amount of more than 10.000.000.

<!-- Your Code Goes Here -->

### 13. All the companies that have been acquired after 2010, ordered by the acquisition amount, retrieving only their `name` and `acquisition` fields.

<!-- Your Code Goes Here -->

### 14. All companies ordered by their `founded year`, retrieving only their `name` and `founded year`.

<!-- Your Code Goes Here -->

### 15. All the companies that have been founded on the first seven days of the month, including the seventh. Sort them by their `acquisition price` in a descending order. Limit the search to 10 documents.

<!-- Your Code Goes Here -->

### 16. All the companies on the 'web' `category` that have more than 4000 employees. Sort them by the amount of employees in ascending order.

<!-- Your Code Goes Here -->

### 17. All the companies whose acquisition amount was more than 10.000.000, and in which the acquisition currency is 'EUR'.

<!-- Your Code Goes Here -->

### 18. All the companies that have been acquired on the first trimester of the year. Limit the search to 10 companies, and retrieve only their `name` and `acquisition` fields.

<!-- Your Code Goes Here -->

### 19. All the companies that have been founded between 2000 and 2010, but have not been acquired before 2011.

<!-- Your Code Goes Here -->
