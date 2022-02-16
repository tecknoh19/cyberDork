# cyberDork
Python3 based Google dork scanner that actually provides link results

Most of the dorkScanners on github pull the CITE tag and do not return useful and readily workable data.  cyberDork serves the need for getting usable results.


usage: cyberDork.py [-h] [-d DORK] [-n NUM_RESULTS] [-o FILENAME] [-c [CHECK_RESULT]]

optional arguments:
  -h, --help            show this help message and exit
  
  -d DORK, --dork DORK  Enter your dork terms in quotes seperated by a space. Ex: "intext:@gmail.com filetype:log"
  
  -n NUM_RESULTS, --num_results NUM_RESULTS
                        Enter the number of results to obtain. Default: 10. Google will cap results at a maximum of
                        100 per query.
                        
  -o FILENAME, --output FILENAME
                        Output results to specified path/file
                        
  -c [CHECK_RESULT], --check_result [CHECK_RESULT]
                        Check link result for HTTP 200 response code

Usage Examples:

python3 cyberDork.py -d "intitle:webcamXP inurl:8080" -n 20 -c
python3 cyberDork.py -d "intitle:index 0f / P intext:index of /" -n 20 -c
python3 cyberDork.py -d "intext:allow filetype.txt" -n 20 -c

