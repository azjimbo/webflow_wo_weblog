This is something I've been playing with for a while.  I noticed that there were flows to my web server that didn't appear in my web logs.  
I exepct this is some sort of vulnerability scanning and thought I should keep an eye on it.  
This weekend I added the avg bytes per packet to see if there was any real data being exchanged.  (not that I can tell so far :) )

I've also included Intrusion_Detection datamodel output of my NIDs to see if there is anything there.  So far, Zeek is showing some (my sourcetypes are still bro in my network) - but if Suricata triggered, that would be there too.  

next, I'll likely add this to my block list so that appearance on this list will result in being blocked by my firewall for 30 days.

You'll need to set up your internal IP space as well as your web server IPs.  I've included comments where they go.

There is a logic issue in here - if an actor checks a web site first, then it won't appear here.  I may correct this later with a time bounding, or using Zeek's flow Id field.  But that's down the road as time permits.

Happy Hunting - 
