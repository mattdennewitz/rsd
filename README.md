# Record Store Day API

Tools to generate a database of record stores from Record Store Day website.

## Tools

### Database generation

To command the data, you must first have the data. Record store locations
are scraped from http://www.recordstoreday.com/ like this:

1. Collect list of venues for each state
   (e.g., http://www.recordstoreday.com/Venues?state=IL)
2. For each venue found, scrape address from Google map.

Out of courtesy, we'll throttle requests to 5/s.

To run,

```bash
$ bin/collect_db
```
