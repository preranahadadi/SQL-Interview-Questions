# SQL Interview Patterns Repository

This repository contains **SQL interview problems from LeetCode and DataLemur** organized by **core SQL patterns**.

---

# 1. Basic SELECT + Filtering

| Problem | Platform | Link |
|------|------|------|
| Recyclable and Low Fat Products | LeetCode | https://leetcode.com/problems/recyclable-and-low-fat-products/ |
| Find Customer Referee | LeetCode | https://leetcode.com/problems/find-customer-referee/ |
| Big Countries | LeetCode | https://leetcode.com/problems/big-countries/ |
| Article Views I | LeetCode | https://leetcode.com/problems/article-views-i/ |
| Invalid Tweets | LeetCode | https://leetcode.com/problems/invalid-tweets/ |
| Not Boring Movies | LeetCode | https://leetcode.com/problems/not-boring-movies/ |
| Fix Names in a Table | LeetCode | https://leetcode.com/problems/fix-names-in-a-table/ |
| Patients With a Condition | LeetCode | https://leetcode.com/problems/patients-with-a-condition/ |
| Find Users With Valid E-Mails | LeetCode | https://leetcode.com/problems/find-users-with-valid-e-mails/ |

Typical pattern

```sql
SELECT *
FROM table
WHERE condition;
```

---

# 2. Joins

| Problem | Platform | Link |
|------|------|------|
| Replace Employee ID With The Unique Identifier | LeetCode | https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/ |
| Product Sales Analysis I | LeetCode | https://leetcode.com/problems/product-sales-analysis-i/ |
| Customer Who Visited but Did Not Make Any Transactions | LeetCode | https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/ |
| Rising Temperature | LeetCode | https://leetcode.com/problems/rising-temperature/ |
| Employee Bonus | LeetCode | https://leetcode.com/problems/employee-bonus/ |
| Students and Examinations | LeetCode | https://leetcode.com/problems/students-and-examinations/ |
| Well Paid Employees | DataLemur | https://datalemur.com/questions/well-paid-employees |
| Page With No Likes | DataLemur | https://datalemur.com/questions/sql-page-with-no-likes |
| Booking Referral Source | Airbnb | https://datalemur.com/questions/booking-referral-source |
| Supercloud Customer | Microsoft | https://datalemur.com/questions/supercloud-customer |

Typical pattern

```sql
SELECT a.col, b.col
FROM tableA a
JOIN tableB b
ON a.id = b.id;
```

---

# 3. Aggregation (GROUP BY)

| Problem | Platform | Link |
|------|------|------|
| Average Selling Price | LeetCode | https://leetcode.com/problems/average-selling-price/ |
| Project Employees I | LeetCode | https://leetcode.com/problems/project-employees-i/ |
| Percentage of Users Attended a Contest | LeetCode | https://leetcode.com/problems/percentage-of-users-attended-a-contest/ |
| Queries Quality and Percentage | LeetCode | https://leetcode.com/problems/queries-quality-and-percentage/ |
| Number of Unique Subjects Taught by Each Teacher | LeetCode | https://leetcode.com/problems/number-of-unique-subjects-taught-by-each-teacher/ |
| Classes With at Least 5 Students | LeetCode | https://leetcode.com/problems/classes-with-at-least-5-students/ |
| Find Followers Count | LeetCode | https://leetcode.com/problems/find-followers-count/ |
| Histogram of Tweets | DataLemur | https://datalemur.com/questions/sql-histogram-tweets |
| Cities With Completed Trades | DataLemur | https://datalemur.com/questions/completed-trades |
| Average Review Ratings | DataLemur | https://datalemur.com/questions/sql-average-review-ratings |
| Teams Power Users | DataLemur | https://datalemur.com/questions/teams-power-users |
| Compressed Mean | DataLemur | https://datalemur.com/questions/compressed-mean |
| Cards Issued Difference | DataLemur | https://datalemur.com/questions/cards-issued-difference |
| Best-Selling Product | Amazon | https://datalemur.com/questions/best-selling-product |
| Histogram of Users and Purchases | Walmart | https://datalemur.com/questions/histogram-users-purchases |
| International Call Percentage | Verizon | https://datalemur.com/questions/international-call-percentage |
| Card Launch Success | JPMorgan | https://datalemur.com/questions/card-launch-success |

Typical pattern

```sql
SELECT column, COUNT(*)
FROM table
GROUP BY column;
```

---

# 4. Conditional Aggregation

| Problem | Platform | Link |
|------|------|------|
| Monthly Transactions I | LeetCode | https://leetcode.com/problems/monthly-transactions-i/ |
| Immediate Food Delivery II | LeetCode | https://leetcode.com/problems/immediate-food-delivery-ii/ |
| Count Salary Categories | LeetCode | https://leetcode.com/problems/count-salary-categories/ |
| App Click-through Rate (CTR) | DataLemur | https://datalemur.com/questions/click-through-rate |
| Laptop vs Mobile Viewership | DataLemur | https://datalemur.com/questions/laptop-mobile-viewership |
| Final Account Balance | DataLemur | https://datalemur.com/questions/final-account-balance |
| Pharmacy Analytics (Part 1) | DataLemur | https://datalemur.com/questions/pharmacy-analytics-part-1 |
| Pharmacy Analytics (Part 2) | DataLemur | https://datalemur.com/questions/pharmacy-analytics-part-2 |
| Pharmacy Analytics (Part 3) | DataLemur | https://datalemur.com/questions/pharmacy-analytics-part-3 |
| Patient Support Analysis (Part 1) | DataLemur | https://datalemur.com/questions/patient-support-analysis-part-1 |
| Patient Support Analysis (Part 2) | UnitedHealth | https://datalemur.com/questions/patient-support-analysis-part-2 |

Typical pattern

```sql
SUM(CASE WHEN condition THEN 1 ELSE 0 END)
```

---

# 5. Duplicate Detection

| Problem | Platform | Link |
|------|------|------|
| Duplicate Job Listings | DataLemur | https://datalemur.com/questions/duplicate-job-listings |
| Delete Duplicate Emails | LeetCode | https://leetcode.com/problems/delete-duplicate-emails/ |

Typical pattern

```sql
GROUP BY column
HAVING COUNT(*) > 1;
```

---

# 6. Subqueries

| Problem | Platform | Link |
|------|------|------|
| Employees Whose Manager Left the Company | LeetCode | https://leetcode.com/problems/employees-whose-manager-left-the-company/ |
| Second Highest Salary | LeetCode | https://leetcode.com/problems/second-highest-salary/ |
| Customers Who Bought All Products | LeetCode | https://leetcode.com/problems/customers-who-bought-all-products/ |

Typical pattern

```sql
SELECT *
FROM table
WHERE column IN (
    SELECT column
    FROM table
);
```

---

# 7. Window Functions

| Problem | Platform | Link |
|------|------|------|
| Game Play Analysis IV | LeetCode | https://leetcode.com/problems/game-play-analysis-iv/ |
| Restaurant Growth | LeetCode | https://leetcode.com/problems/restaurant-growth/ |
| Friend Requests II | LeetCode | https://leetcode.com/problems/friend-requests-ii-who-has-the-most-friends/ |
| Department Top Three Salaries | LeetCode | https://leetcode.com/problems/department-top-three-salaries/ |
| User's Third Transaction | DataLemur | https://datalemur.com/questions/users-third-transaction |
| Second Day Confirmation | DataLemur | https://datalemur.com/questions/second-day-confirmation |
| User Shopping Sprees | Amazon | https://datalemur.com/questions/user-shopping-sprees |
| 2nd Ride Delay | Uber | https://datalemur.com/questions/second-ride-delay |

Typical pattern

```sql
ROW_NUMBER() OVER (PARTITION BY column ORDER BY column)
```

---

# 8. Date / Time Analysis

| Problem | Platform | Link |
|------|------|------|
| Product Price at a Given Date | LeetCode | https://leetcode.com/problems/product-price-at-a-given-date/ |
| Average Post Hiatus | DataLemur | https://datalemur.com/questions/sql-average-post-hiatus |
| Odd and Even Measurements | Google | https://datalemur.com/questions/odd-even-measurements |

Typical pattern

```sql
DATEDIFF(date1, date2)
```

---

# 9. Data Transformation

| Problem | Platform | Link |
|------|------|------|
| Exchange Seats | LeetCode | https://leetcode.com/problems/exchange-seats/ |
| Consecutive Numbers | LeetCode | https://leetcode.com/problems/consecutive-numbers/ |
| Triangle Judgement | LeetCode | https://leetcode.com/problems/triangle-judgement/ |
| Last Person to Fit in the Bus | LeetCode | https://leetcode.com/problems/last-person-to-fit-in-the-bus/ |
| Investments in 2016 | LeetCode | https://leetcode.com/problems/investments-in-2016/ |
| Group Sold Products By The Date | LeetCode | https://leetcode.com/problems/group-sold-products-by-the-date/ |
| List the Products Ordered in a Period | LeetCode | https://leetcode.com/problems/list-the-products-ordered-in-a-period/ |
| IBM db2 Product Analytics | DataLemur | https://datalemur.com/questions/ibm-db2-product-analytics |
| QuickBooks vs TurboTax | DataLemur | https://datalemur.com/questions/quickbooks-vs-turbotax |
| Swapped Food Delivery | Zomato | https://datalemur.com/questions/swapped-food-delivery |
| Compressed Mode | Alibaba | https://datalemur.com/questions/compressed-mode |
| FAANG Stock Min-Max (Part 1) | Bloomberg | https://datalemur.com/questions/faang-stock-min-max |
| Google Maps Flagged UGC | Google | https://datalemur.com/questions/google-maps-flagged-ugc |

---

# Core SQL Interview Patterns

1. Basic Filtering (WHERE)  
2. Joins  
3. Aggregation (GROUP BY)  
4. Conditional Aggregation  
5. Duplicate Detection  
6. Subqueries  
7. Window Functions  
8. Date / Time Problems  
9. Data Transformation  

Mastering these patterns solves **80–90% of SQL interview questions**.
