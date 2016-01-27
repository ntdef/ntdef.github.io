---
title: Taming ~/Downloads with cron and find
---

I'm going to go out on a limb and say you have a Downloads folder problem. I certainly do. I regularly rack up 20 gigabytes worth of stuff just accumulating there with the (false) hopes of one day getting around to those saved articles, libraries and other debris off the interwebs. For me, it was a matter of coming to terms with the fact that I'm never going to touch that stuff. 

It was a thought reaffirmed to me while reading [a book on tidying up](http://amzn.com/B00KK0PICK) where the author notes that many people she consulted with accumulated books with the intention to read them, but seldmom did. The best opportunity to read something is when its first presented to you: later on its more likely to fall by the wayside. 

The same goes for downloads. I would find myself dowloading files with the intention to look over them later only to find time grow too scarce. And so to force myself to confront the inevitable with new material, I added the following line to my cron tab:

```
# Runs every day at 5:45 pm
45 17 * * * ntdef find ~/Downloads \( -type d -or -type f \) -mtime +1 -delete
```

I use `find` to lookup all files and directories that are older than one day and delete any files found matching that criteria. That way if I come across an interesting article I'm forced to either look at it then and there or take the time to make a judgment about how mission-critical it actually is. Now I find myself being more discerning about what things I take on and dealing less with information overload.

It's funny how a cron job can change your perspective on things. 
