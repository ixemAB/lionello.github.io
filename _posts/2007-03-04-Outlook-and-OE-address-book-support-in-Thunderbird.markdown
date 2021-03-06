---
layout: post
title: Outlook and OE address book support in Thunderbird
categories:
- Knowledge Base
permalink: /archives/5-Outlook-and-OE-address-book-support-in-Thunderbird.html
s9y_link: http://www.lunesu.com/index.php?/archives/5-Outlook-and-OE-address-book-support-in-Thunderbird.html
date: 2007-03-04 08:17:00.000000000 +08:00
---
From <a href="http://ilias.ca/blog/2006/03/outlook-and-oe-address-book-support-in-thunderbird/" title="Chris Ilias' Blog">Chris Ilias' Blog</a>:

To make Thunderbird use your Outlook Express address book, close Thunderbird, and add the following lines to your prefs.js file:
{% highlight sh %}
user_pref("ldap_2.servers.OE.description", "Outlook Express");
user_pref("ldap_2.servers.OE.dirType", 3);
user_pref("ldap_2.servers.OE.uri", "moz-aboutlookdirectory://oe/");
{% endhighlight %}

For Outlook Contacts, use these lines:
{% highlight sh %}
user_pref("ldap_2.servers.Outlook.description", "Outlook");
user_pref("ldap_2.servers.Outlook.dirType", 3);
user_pref("ldap_2.servers.Outlook.uri", "moz-aboutlookdirectory://op/");
{% endhighlight %}
One important note: in order for it to work with Outlook, Outlook must be set as the system default mail client.
