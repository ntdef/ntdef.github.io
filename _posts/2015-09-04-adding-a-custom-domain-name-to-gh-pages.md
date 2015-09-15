---
title: How to use your NameCheap domain name on Github Pages
---

 Clearly, static blogs are all the rage these days, especially since you can
host your blog for free on github pages. It's simply a breeze.

 However, getting my personal domain name to appear on the site was a bit
tricky. I was suddenly receiving infinite redirect loop errors whenever I tried
visiting my blog. The problem, as I later found out, was how I had set up
domain forwarding on NameCheap.  

## NameCheap Forwarding Done Right
 Assuming that you've [added a CNAME file at the root of your
 repo](https://help.github.com/articles/tips-for-configuring-a-cname-record-with-your-dns-provider/), to set
up your NameCheap domain to forward properly to github pages, **do not** use
the forwarding link in the sidebar. This was my first mistake: even though it
seems like the right option, the configuration options NameCheap provides in
that view are too limited for setting up forwarding to GitHub. Instead navigate
to `All Host Records` which has more fields for adding the appropriate IP
addresses.  

 ![namecheap-ghpages-1](/assets/images/namecheap-ghpages-1.png)

  To set up forwarding you need to add two static IP destinations that GitHub
 provides
 [here](https://help.github.com/articles/my-custom-domain-isn-t-working/#dns-errors)
 which should be the same as the ones listed below.

 ![namecheap-ghpages-2](/assets/images/namecheap-ghpages-2.png)


## Other Possible Pitfalls
 - Don't specify the protocol in the CNAME file. Just omit the `http://` prefix and you'll be fine.
 - For the CNAME record type in NameCheap's portal, the trailing period is added automatically and is harmless.
