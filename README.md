# Worklog
A simple CLI for logging work.

# Install Worklog
Save the worklog file from this repo on your system in handy location, perhaps `/usr/local/bin`:

        wget https://raw.githubusercontent.com/managedkaos/worklog/master/worklog -O /usr/local/bin/worklog

Then add the following to your .bashrc:

        source /usr/local/bin/worklog

# Use Worklog
Log a work entry with the following format:

        worklog ORG_NAME "Log Message"

Where ORG_NAME is the name of the organization you did the work for and "Log Message" is what you'd like to log.

For example:

        worklog Google "Today I linted a bunch of python for google"
        worklog Facebook "I also linted for facebook"
        worklog Disney "Working here was magical"
        worklog Amazon "I did some shopping on amazon"

Logs are stored in your home directory in the `.worklog` directory.  A new log file is created for each day that you submit a log.

You can view the logs like this:

        reportlog

        2018-09-17 20:01:15    Google    "Today I linted a bunch of python for google"
        2018-09-17 20:01:16    Facebook    "I also linted for facebook"
        2018-09-17 20:01:16    Disney    "Working here was magical"
        2018-09-18 20:01:16    Amazon    "I did some shopping on amazon"

To search the log, you can add a case insensitive search term to `reportlog`:

        reportlog google

        2018-09-17 20:01:15    Google    "Today I linted a bunch of python for google"

Or to see the log for a particular day, search on that date

        reportlog 09-18

        2018-09-18 20:01:16    Amazon    "I did some shopping on amazon"
