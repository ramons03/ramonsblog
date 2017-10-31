title: Save instead of send email for testing
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-09-14 11:54:30
tags:
---
* [MSDN: <specifiedPickupDirectory> Element (Network Settings)](https://docs.microsoft.com/en-us/dotnet/framework/configure-apps/file-schema/network/specifiedpickupdirectory-element-network-settings)
* [Configuring SmtpClient to drop emails in a folder on disk](http://mikehadlow.blogspot.com.ar/2010/01/configuring-smtpclient-to-drop-emails.html)
```xml
<system.net>
  <mailSettings>
    <smtp deliveryMethod="SpecifiedPickupDirectory">
      <specifiedPickupDirectory pickupDirectoryLocation="c:\Temp\mail\"/>
    </smtp>
  </mailSettings>
</system.net>
```