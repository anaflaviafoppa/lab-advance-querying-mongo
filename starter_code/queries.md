![Ironhack Logo](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Answers

### 1. All the companies whose name match 'Babelgum'. Retrieve only their `name` field.

<!-- Your Code Goes Here -->

{
filter:{"name":{"\$eq":"Babelgum"}}
sort:
limit:
}

{
\_id: 52cdef7c4bab8bd675297da0
name:"Babelgum"
permalink:"babelgum"
}

### 2. All the companies that have more than 5000 employees. Limit the search to 20 companies and sort them by **number of employees**.

<!-- Your Code Goes Here -->

{
filter:{"number_of_employees":{"\$gt":5000}}
sort: {"number_of_employees": 1}
limit: 20
}

### 3. All the companies founded between 2000 and 2005, both years included. Retrieve only the `name` and `founded_year` fields.

<!-- Your Code Goes Here -->

{
filter:{"$and":[{"founded_year": {"$gte":2000}},{"founded_year":{"\$lte":2005}}]}
sort: {"name":1}
limit:
}

{
\_id:52cdef7f4bab8bd67529c5b0
name:10East
founded_year:2002
}

{
\_id:52cdef7d4bab8bd675298e7e
name: 1915 Studios
founded_year:2004
}

### 4. All the companies that had a Valuation Amount of more than 100.000.000, and have been founded before 2010. Retrieve only the `name` and `ipo` fields.

<!-- Your Code Goes Here -->

{
filter:{"$and":[{"ipo.valuation_amount":{"$gte":100000000}},{"founded_year":{"\$lte":2010}}]}
sort: {"name":1}
limit:
}

<!--First two - 42 documents-->

{
\_id:52cdef7c4bab8bd675297e7a
name:"Amazon"
founded_year:1994
}
{
id:52cdef7c4bab8bd675298760
name: "Baidu"
founded_year:1999
}

### 5. All the companies that have less than 1000 employees and have been founded before 2005. Order them by the number of employees and limit the search to 10 companies.

<!-- Your Code Goes Here -->

{
filter:{"$and":[{"number_of_employees":{"$lt":1000}},{"founded_year":{"\$lte":2005}}]}
sort: {"number_of_employees":1}
limit: 10
}

<!--First two - 10 documents-->

{
\_id:52cdef7c4bab8bd675297d93
name:"Fox Interactive Media"
founded_year:1979
}

{
\_id:52cdef7c4bab8bd675297dbc
name:"Skype"
founded_year:2003
}

### 6. All the companies that don't include the `partners` field.

<!-- Your Code Goes Here -->

{
filter:{"partners":{"\$exists":false}}
sort:
limit:
}

<!-- 0 document-->

### 7. All the companies that have a null value on the `category_code` field.

<!-- Your Code Goes Here -->

{
filter:{"category_code":{"\$in":[null]}}
sort:
limit:
}

<!-- 2751 documents-->

{
"name": "Collective",
"category_code": null,
},

{
"name": "Snimmer",
"category_code": null,
}

### 8. All the companies that have at least 100 employees but less than 1000. Retrieve only the `name` and `number of employees` fields.

<!-- Your Code Goes Here -->

{
filter:{"$and":[{"number_of_employees":{"$gte":100}}, {"number_of_employees":{"\$lte":1000}}]}
sort: {"name":1}
limit:
}

<!-- 942 documents-->

{
"name": "2 Minutes",
"number_of_employees": "105"
}

### 9. All the companies ordered by their IPO price in a descending manner.

<!-- Your Code Goes Here -->

{
filter:{"ipo":{"\$exists":true}}
sort: {"ipo.valuation_amount":-1}
limit:
}

<!-- 18798 documents-->

{
name:"GREE"
ipo:
valuation_amount:108960000000
valuation_currency_code:"JPY"
pub_year:2008
pub_month:12
pub_day:17
stock_symbol:"3632"
}

### 10. The 10 companies with the highest amount of employees, order by the `number of employees`.

<!-- Your Code Goes Here -->

{
filter:
sort: {"number_of_employees":-1}
limit: 10
}

{
name:"Siemens"
number_of_employees:405000
},
{
name:"IBM"
number_of_employees:388000
},
{
name:"Toyota"
number_of_employees:320000
},

### 11. All the companies founded on the second semester of the year. Limit your search to 1000 companies.

<!-- Your Code Goes Here -->

{
filter: {"$and":[{"founded_month":{"$nin":[null]}},{"founded_month":{"\$gte":7}}]}
sort:
limit: 1000
}

### 12. All the companies founded before 2000 that have an acquisition amount of more than 10.000.000.

<!-- Your Code Goes Here -->

{
filter: {"$and":[{"acquisitions.price_amount":{"$gte":10000000}},{"founded_year":{"\$lte":2000}}]}
sort:
limit: 0
}

<!-- 286 companies -->

### 13. All the companies that have been acquired after 2010, ordered by the acquisition amount, retrieving only their `name` and `acquisition` fields.

<!-- Your Code Goes Here -->

{
filter: {"acquisitions.acquired_year":{"\$gt":2010}}
sort: {"acquisitions.price_amount":-1}
limit: 0
}

<!-- 665 companies -->

### 14. All companies ordered by their `founded year`, retrieving only their `name` and `founded year`.

<!-- Your Code Goes Here -->

{
filter: {"founded_year":{"\$nin":[null]}}
sort: {"founded_year":1}
limit: 0
}

### 15. All the companies that have been founded on the first seven days of the month, including the seventh. Sort them by their `acquisition price` in a descending order. Limit the search to 10 documents.

<!-- Your Code Goes Here -->

{
filter: {"founded_day":{"\$lte":7}}
sort: {"acquisition.price_amount":-1}
limit: 0
}

### 16. All the companies on the 'web' `category` that have more than 4000 employees. Sort them by the amount of employees in ascending order.

<!-- Your Code Goes Here -->

{
filter: {"$and":[{"category_code":{"$in":["web"]}},{"number_of_employees":{"\$gt":4000}}]}
sort: {"number_of_employees":-1}
limit: 0
}

### 17. All the companies whose acquisition amount was more than 10.000.000, and in which the acquisition currency is 'EUR'.

<!-- Your Code Goes Here -->

{
filter:{"$and":[{"acquisition.price_amount":{"$gt":10000000}},{"acquisition.price_currency_code":{"\$in":["EUR"]}}]}
sort:
limit: 0
}

<!-- 7 companies -->

### 18. All the companies that have been acquired on the first trimester of the year. Limit the search to 10 companies, and retrieve only their `name` and `acquisition` fields.

<!-- Your Code Goes Here -->

{
filter:{"acquisition.acquired_month":{"\$lte":3}}
sort:
limit: 10
}

### 19. All the companies that have been founded between 2000 and 2010, but have not been acquired before 2011.

<!-- Your Code Goes Here -->

{
filter:{"$and":[{"founded_year":{"$gte":2000}},{"founded_year":{"\$lte":2011}}]}
sort:
limit: 0
}

<!-- 10699 companies -->
