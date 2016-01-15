# Amazon Dash + One Button Uber Automation

> Hack the Amazon Dash Button to Call an Uber while you pregame... or whatever other people do before an Uber.

```
Author: Trevor Davenport
```
![](http://i.imgur.com/ziyfHNP.png)
#### Background ####
```
  Amazon Dash: www.amazon.com/oc/dash-button
  Credits: https://medium.com/@edwardbenson/how-i-hacked-amazon-s-5-wifi-button-to-track-baby-data-794214b0bdd8
```
___

#### Overview ####
![](http://i.imgur.com/qsnLNB1.jpg)
![](http://i.imgur.com/V3WZ72E.jpg)
___

### Setting Up Your Dash Button ###

![](http://i.imgur.com/ubeiy9U.png)

#### Sniffing ARP Probes ####
```
  1. Run dash_sniff.py, Push Dash Button, Wait for print response
  2. Note and Save MAC Address of Dash Button.
  3. We will hardcode this MAC Address into our main program.
```
```python
  #Sniff Dash ARP Probes (dash_sniff.py)
  from scapy.all import *
  def arp_display(pkt):
    if pkt[ARP].op == 1: #who-has (request)
      if pkt[ARP].psrc == '0.0.0.0': # ARP Probe
        print "ARP Probe from: " + pkt[ARP].hwsrc
  print sniff(prn=arp_display, filter="arp", store=0, count=10)
```

___

### Shodan API ###
###### Service to Port Shodan Mapping ######


