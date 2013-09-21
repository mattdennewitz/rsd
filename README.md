# Record Store Day API

Tools to generate a database of record stores from Record Store Day website.

## Tools

### Database generation

To command the data, you must first have the data. Record store locations
are scraped from http://www.recordstoreday.com/ like this:

#### Collect list of venues for each state

First, we need to scrape a list of venues for each region (states, countries).
To do this, use `collect_venues`, which will scrape a list of URLs.

```bash
$ bin/collect_venues -c /path/to/config.json [-o /path/to/output.csv]
```

Arguments:

- `-c` - Path to JSON configuration file. A sample configuration file is included
         with this project. **Required.**
- `-o` - Export path for CSV list of venue urls. Default: stdout.

#### Scrape addresses for each venue

