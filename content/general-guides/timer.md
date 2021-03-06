---
linktitle: Timer syntax
title: Timer specification
highlight: true
weight: 9
---

Each job in reef-pi is executed at a given schedule. A job's schedule specifies day and time related details.

reef-pi uses [cron](https://en.wikipedia.org/wiki/Cron) like specification to define job schedules.

Following is a summary of the specification

- "day of month" represent which day of every month the job will be triggered. Values can range from 1 to 31
- "hour" represent which hour of the day job will be triggered. Values can range from 0 to 23
- "minute" represent which minute of the hour job will be triggered. Value can range from 0 to 59
- "second" represent which second of the minute job will be triggered. Values can range from 0 to 59


Other than their mentioned ranges, each of this field can also take few special entries.

They are:

- "\*" represents **every** . Like every hour, every day etc
- "-" to represent **ranges**. Example: hour can be "2-6" to trigger a job every hour from 2 to 6
- "/" to represent **after every**. Example: Hour value "\*/3" represents after every 3 hours

More details can be found in  the underlying library's [documentation](https://godoc.org/github.com/robfig/cron#hdr-CRON_Expression_Format)
