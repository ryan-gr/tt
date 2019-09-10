# tt

### Purpose

tt is a simple command-line utility to track work done for a single project. 
It ouputs the number of hours worked per day, carrying over minutes over to the next day, until they can be accumulated into another hour. 

### Usage

tt follows a simple workflow, typically `tt -s` is used to signal the start of a session, while `tt -e` is used to signal an end of a session.
To specify a start or end time, one could also use `tt -s 1400` or `tt -e 1500`. 
> When using a 24-hour time format, having a start time on one day and an end on the next day automatically closes the time on the previous day, and opens a new time at midnight for the next day.

If a new record is needed (for example, if a fresh timesheet is going to be used), use the `tt -n` command to create a new session. Each session is stored in a `.tsh` file, stored in the same folder as the utility. A new `.tsh` file will be created and used subsequently.

Use `tt -m` to modify the current `.tsh` file to manually edit entries.

The `tt -p` command can be used to parse the current `.tsh` file, showing you the number of hours worked per day, and the total number of hours of work recorded.
