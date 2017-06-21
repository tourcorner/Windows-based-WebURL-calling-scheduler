# Windows scheduler with running in auto service
Simple scheduler like Cron created using VB.NET. we can use url to execute in interval

We can use this as windows service without login to system.

keep these 2 files in one folder

BHITimeLogSync.exe
<br />
settings.xml

and change the URL in the xml and time interval in sec.

Now 5000 is milli seconds. its 5 seconds.

you can increase or decrease too. 
<h1>settings.xml</h1>

&lt;?xml version="1.0" encoding="utf-8"?&gt;<br />
&lt;root&gt;<br />
&lt;file&gt;<br />
    &lt;scriptpath&gt;http://localhost/yourphpfile.php?querystring=1&lt;/scriptpath&gt;<br />
	&lt;interval>5000&lt;/interval&gt;<br />
&lt;/file&gt;<br />
&lt;/root&gt;<br />

<h1>install as service</h1>
open your command prompt (run as <b>Administrator</b>)

cd C:\Windows\Microsoft.NET\Framework64\v4.0.30319\

<b>installutil path/to/BHITimeLogSync.exe</b>

<h1>UnInstall service</h1>

<b>installutil /u path/to/BHITimeLogSync.exe</b>

