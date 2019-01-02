---
title: New Year's DNS Resolution
date: 2019-01-02T00:52:56.206Z
tags:
  - dns
  - en
---
One of the good things that you get when you have your own domain is that you can experiment with any crazy idea that comes to your mind, when it comes to publishing content.

So why not use a DNS server to keep the New Year's resolution? After all, the DNS server is there for resolutions (pun intended).

The DNS sysmtems have the hability to keep TXT records, and domain administrators use them to setup mail protection (SPF, DMARC, DKIM), to valided the domain ownership when siging a new service. Some of them also add entries with the slogan of a company or the company's name.

So, I decided to make a short new year's resolution list, and make it public available in my domain as a TXT record. The list must be short as the TXT records can only hold 255 ASCII printable characters. This link from [Bind 9 Configuration and Setup](https://kb.isc.org/docs/aa-00356), describes a way to create a record with more than 255 characters but I have not tested it. I might increase the list later when I have time and see how well it will work.

I also decided to write the resolution list in English, as to make it in Portuguese or Spanish, I would have look for words that don't have accent marks.

At this point you might be wondering how you can see my new year's resolution list.

There are two methods to see the list:

* Check this link from [MX Toolbox](https://mxtoolbox.com/SuperTool.aspx?action=txt%3a2019.silvino.net&run=toolpage#)
* Or open your Command Prompt. Type "nslookup -q=txt 2019.silvino.net"

That's all. I hope you liked it!
