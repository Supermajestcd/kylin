---
layout: docs40
title:  Quick Start with Sample Cube
categories: tutorial
permalink: /docs40/tutorial/kylin_sample.html
---

Kylin provides a script for you to create a sample Cube; the script will also create five sample Hive tables:

1. Run `${KYLIN_HOME}/bin/sample.sh`; Restart Kylin server to flush the caches;
2. Logon Kylin web with default user and password ADMIN/KYLIN, select project `learn_kylin` in the project dropdown list (left upper corner);
3. Select the sample Cube `kylin_sales_cube`, click "Actions" -> "Build", pick up a date later than 2014-01-01 (to cover all 10000 sample records);
4. Check the build progress in the "Monitor" tab, until 100%;
5. Execute SQLs in the "Insight" tab, for example:

```
select part_dt, sum(price) as total_sold, count(distinct seller_id) as sellers from kylin_sales group by part_dt order by part_dt
```

 6.You can verify the query result and compare the response time with Hive;
 
## What's next

You can create another Cube with the sample tables, by following the tutorials.