# reporter
Neo4J Cypher Script

Parses a csv file obtained from the excellent Reporter&copy; app.

The general scheme is:

```
(Report)  - [:REPORTED_ON_DAY]  -> (Day)
(Day)     - [:IN_MONTH]         -> (Month)
(Month)   - [:IN_YEAR]          -> (Year)
(Report)  - [:WAS_WITH]         -> (Person)
(Report)  - [:WAS_DOING]        -> (Activity)
```

Challenges were splitting fields into multiple values, handling null values, and creating unique nodes for people, time, and activities.

I made a gist for seeing the thing in action:
http://gist.neo4j.org/?aba998f750a9fa5c5584

based on https://gist.github.com/joesus/aba998f750a9fa5c5584
