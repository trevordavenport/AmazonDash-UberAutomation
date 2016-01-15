# Amazon Dash Button + Automating Uber

===========================
> Hack the Amazon Dash Button to Call an Uber while you pregame... or whatever other people do before an Uber.

```
Author: Trevor Davenport
```

#### Background ####
```
  Masscan Port Scanner: https://github.com/robertdavidgraham/masscan
  Masscan Man Page:     http://manpages.ubuntu.com/manpages/vivid/man8/masscan.8.html
  
  Python Dependencies: Requests (http://www.python-requests.org/en/latest/)
                       BeautifulSoup (http://www.crummy.com/software/BeautifulSoup/)
                       Shodan API (https://shodan.readthedocs.org/en/latest/)
                       
  Other Dependencies: CURL (http://curl.haxx.se/)
```
___

#### Overview ####
```
 1  [*] Masscan initiates port scan
 2   [*] Results are generated in XML output
 3    [*] Output is pushed to scanhub.shodan.io/repo
 4     [*] Data Analysis for Security/Vulnerability Management
```
___

#### Usage ####

![](http://i.imgur.com/cFcey2H.png)

___

### Shodan API ###
###### Service to Port Shodan Mapping ######
  Shodan Provides a dictionary of common Ports to known Services, we can use this data to further expand the knowledge of our open port list.


