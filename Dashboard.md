

----
## To Apply
----
```dataview
table  location, company 
from "Offers"
where   !applied  
```

----
## In Flight Waiting for Reply
----
```dataview
table  location, company
from "Offers"
where applied and !first_interview_planned and !rejected and !abandonment
sort application_date asc
```

----
## First interview planned
----
```dataview
table  location, company
from "Offers"
where first_interview_planned  and !first_interview_passed and !rejected and !abandonment
sort application_date asc
```

----
## First interview passed and on going
----
```dataview
table  location, company
from "Offers"
where first_interview_passed and !second_interview_planned and !rejected and !abandonment
sort application_date asc
```
----
## Second interview passed and on going
----
```dataview
table  location, company
from "Offers"
where second_interview_passed and !rejected  and !abandonment
sort application_date asc
```

----
## Dropped  because rejected
----

```dataview
table company as "Company Link"
from "Offers"
where rejected
sort application_date asc
```

----
## Dropped because gave up
----
```dataview
table company as "Company Link",  reasons_abandonment
from "Offers"
where abandonment
sort application_date asc
```

---