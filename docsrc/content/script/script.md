---
title: Script
menu:
  main:
      parent: Script
      identifier: script
      weight: 301
---


Now that you have your Public IP address you can access a few different apps that you can leverage:
* Trending Now Dashboard - <http://publicIP:8081/>
* Zeppelin Notebook - <http://publicIP::8080/>
* DataStax OpsCenter - <http://publicIP:8888/>
* Solr Admin UI - <http://publicIP:8983/solr/>

---

## Sketching Application

### Trending Now Dashboard 
This is your screen to walk users through the visualization of the demo. It consist of three seperate windows.
#### Perspective 10 seconds
This view is showing the raw processing of the twitter feed. Breaking down each 10 second streaming window into Hyperloglog and countminsketch data structures. This view does not have trending hashtags because its not as vaulable within 10 seconds.
#### Perspective 10 minutes
This view is showing a 'roll-up' sketch of 10 second windows into 10 minute windows. Each point represents 10 minutes and since our sketching datastuctures has associative properties, this is not merely a simple count, but a representation of unique users over ten minutes. Additionally, we have a view of top hashtags. This uses countminsketch to create a frequency of hashtags seen on incomming tweets. You are able to click these and view them on twitter. 
#### Architecture Window
##### Logical Architecture
This diagram demonstates how the application works. It communicates the flow of data through the system and the creation of multiple perspectives.  
##### Physical Architecture
A future state architecute outlining the various components of the architecture.

### Zeppelin Notebook 
The Zeppelin notebook contains scala code samples to build query results. This offers the ability to build some dynamic queries for the demo. Contains samples for countmin sketch and hyperloglog

### OpsCenter
If needed for your demo, you can access OpsCenter and give a tour of it at <http://publicIP:8888/>:

