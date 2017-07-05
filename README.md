# CheckPwnedList
A modification of a script that takes a single email, or a file with multiple emails and checks the have i been pwned site.

Improvments from original: Updated headers.  The output file is a Tab Delimited file that can be opened in Excel or any similar software.


This python script will check if a single email address, or a text file listing several email addresses, has been compromised in a data breach (pwned).  This script uses the haveibeenpwned API to compare the email address(es), provided by the user, to the haveibeenpwned database to check if they have been pwned or not.


To check a single email address:

```
python checkpwnedemails.py -s email_address
```

To check multiple email address:

```
python checkpwnedemails.py -i text_file_listing_email_addresses
```

By default, the results will be printed to standard output.  However, if the -o option is provided, the output data will be printed to a tab delimited textfile for later use.

For more options:

```
python checkpwnedemails.py -h
```


To convert to proper csv for excel 2 steps required.

1. in vim: `%s/\\',\\ /\\ /g`

replace <hit tab key> by physically deleting that string and pushing the tab button

2.in vim: `%s/\\<hit tab key>/,\\ /g`     

