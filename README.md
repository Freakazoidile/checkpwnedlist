# CheckPwnedList
A modification of a modification of a script that takes a single email, or a file with multiple emails and checks the have i been pwned site.

Improvments: Updated headers.  The output file is a Tab Delimited file that can be opened in Excel or any similar software.

# Usages Examples
```
./HaveTheyBeenPwned.py -h
usage: HaveTheyBeenPwned.py [-h] [-i INPUT_PATH] [-o OUTPUT_PATH]
                            [-oR OUTPUT_PATH_REPORT] [-oX OUTPUT_XML]
                            [-s RATE_LIMIT_SLEEP]

optional arguments:
  -h, --help            show this help message and exit
  -i INPUT_PATH         Path to text file that lists email addresses.
  -o OUTPUT_PATH        Path to output to text file.
  -oR OUTPUT_PATH_REPORT
                        Path to output to text file in report ready format.
  -oX OUTPUT_XML        Path to output to XML file.
  -s RATE_LIMIT_SLEEP   Obey the rate limit of the API.
```

Simplest method to seach for all emails in emails.txt and output the results to screen, no rate limit rule but if it hits the rate limit error that entry will be excluded from the results.
```
./HaveTheyBeenPwned.py -i emails.txt 
```

To search HIBP for all emails in emails.txt and output the results as seen on screen to found.txt, tries one entry from emails.txt every 1.6 seconds.
```
./HaveTheyBeenPwned.py -i emails.txt -o found.txt -s 1.6
```

To search HIBP for all eamils in emails.txt and output the results to found.txt prefixing each line with a dash (-), tries one entry from emails.txt evert 1.6 seconds.
```
./HaveTheyBeenPwned.py -i emails.txt -oR found.txt -s 1.6
```

