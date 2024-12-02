This is something I've been playing with for a while.  I noticed that there were flows to my web server that didn't appear in my web logs.  
I exepct this is some sort of vulnerability scanning and thought I should keep an eye on it.  
This weekend I added the avg bytes per packet to see if there was any real data being exchanged.  (not that I can tell so far :) )

I've also included Intrusion_Detection datamodel output of my NIDs to see if there is anything there.  So far, Zeek is showing some (my sourcetypes are still bro in my network) - but if Suricata triggered, that would be there too.  

I have this on a dashboard with other exerpimental web server related hunting things so I can check it out as the mood hits.   

Next, I'll likely turn it in to a recurring query and add the results to my block list process. Appearance on this list will result in being blocked by my firewall for 30 days.

You'll need to set up your internal IP space as well as your web server IPs.  I've included comments where they go.

There is a logic issue in here - if an actor checks a web site first, then it won't appear here.  I may correct this later with a time bounding, or using Zeek's flow Id field.  But that's down the road as time permits.

And, as time permits, I might also experiment with other open ports - but I don't have many ports open :) 

With much of my stuff, this is a work in progress.

Happy Hunting - 
