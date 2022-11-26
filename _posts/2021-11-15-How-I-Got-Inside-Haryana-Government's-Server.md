---
id: "hmH5ZBvNwkCfm4V08Kvol"
title: "How I Got Inside Haryana Government's Server"
desc: ''
updated: "1636922485909"
created: "1636922485909"
date: "2021-11-15"
categories: 
  - "research"
date: "'2020-05-16'"
categories:
  - research
---

I found https://onemapggm.mcg.gov.in/server/rest/services was open. This link caters as a REST API used for numerous services for monitoring and recording Harayana's municipal information such as categorisations of wards to various people alongwith their details, list of registered business/industrial entities, COVID-19 emergency pass issuance-removal and other records, traffic challan details of offenders with their personal information such as mobile, aadhar, address, vehicle number, penalty amount, payment mode, etc.

Also database relating to all properties registered/vacant in Harayan were present alongwith their exact location(lat-long) and their unique codes which further could be used to find information relating to person to whom the property is registered.

 

All this information was open for all to see, even the complaints filed, feedback given were accessible openly exposing all details of citizens.

 

Once i found this portal, i had to customise SQL query to return all fields, which is pretty old trick by putting a condition that evaluates to True no matter what, hence "1=1" and return fields must be "\*" to get all data stored on table in database.

Somehow their default configuration has set max records to 1000, hence need to write a script which routes requests via Tor protocol and get all data in tranches of 1000.

 

Screen Captures:
