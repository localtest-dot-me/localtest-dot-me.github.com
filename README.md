localtest.me
================

Credits: Scott Forsyth, Imar Spaanjaars, others

Save this URL, memorize it, write it on a sticky note, tweet it, tell your colleagues about it! 

localtest.me (http://localtest.me)

and

*.localtest.me (http://something.localtest.me)

If you do any testing on your local system you’ve probably created hosts file entries (c:\windows\system32\drivers\etc\hosts) for different testing domains and had them point back to 127.0.0.1.  This works great but it requires just a bit of extra effort.

This localtest.me trick is so obvious, so simple, and yet so powerful.  I wouldn’t be surprised if there are other domain names like this out there, but I haven’t run across them yet so I just ordered the domain name localtest.me which I’ll keep available for the internet community to use.

Here’s how it works. The entire domain name localtest.me—and all wildcard entries—point to 127.0.0.1.  So without any changes to your host file you can immediate start testing with a local URL.

Examples:

    http://localtest.me 
    http://newyork.localtest.me 
    http://mysite.localtest.me 
    http://redirecttest.localtest.me 
    http://sub1.sub2.sub3.localtest.me

You name it, just use any *.localtest.me URL that you dream up and it will work for testing on your local system.

Troubleshooting
================
Your network may have DNS rebinding protection enabled. If so then lookups to `localtest.me` will be unresolved. Quick check: Run `nslookup localtest.me`, if the output does not contain 127.0.0.1 then something in your network is filtering the domain resolution.

Here's a few possible fixes

1. Check your router configuration for DNS rebinding protection. It may be possible to add an exception for `localtest.me`.
2. Configure your host to use an alternative DNS provider such as [Cloudflare 1.1.1.1](https://developers.cloudflare.com/1.1.1.1/setup/) or [Google 8.8.8.8](https://developers.google.com/speed/public-dns/docs/using).

For more information, see the Wikipedia article on [DNS rebinding](https://en.wikipedia.org/wiki/DNS_rebinding).

More details
================

Read the introduction by [Scott Forsyth](http://weblogs.asp.net/owscott/archive/2012/05/14/introducing-testing-domain-localtest-me.aspx)
