---
inFeed: true
description: >-
  Sooo.. umm last post we set up a custom domain name.. and then went all
  stitcher / nsa and added SSL to our domain.. S’rsly bad ass plan.. but wtf..
  we forgot about an email account for our new site…
dateModified: '2017-09-07T11:49:09.053Z'
datePublished: '2017-09-07T11:49:09.583Z'
title: part deux.. wtf i don’t have an email account..
author: []
publisher: {}
via: {}
hasPage: true
sourcePath: _posts/2017-09-02-part-deux-wtf-i-dont-have-an-email-account.md
starred: false
datePublishedOriginal: '2017-09-02T21:18:27.229Z'
url: part-deux-wtf-i-dont-have-an-email-account/index.html
_type: Article

---
# part deux.. wtf i don't have an email account..

Sooo.. umm last post we set up a custom domain name.. and then went all stitcher / nsa and added SSL to our domain.. S'rsly bad ass plan.. but wtf.. we forgot about an email account for our new site...
![](https://s3-us-west-2.amazonaws.com/the-grid-img/p/7bdca4b10c3690b9a085c06de50a80fad3b8beb5.jpg)

> "I would have absolutely messed up 'The Matrix'." ~ Will Smith

..ehhm we just did .. most domain providers will offer email hosting with your new custom domain.. but we f\*&k'd up.. we changed the control to Cloudflare.. soo umm we need a 3rd party....

Gone are the days of gmail for custom domains.. well actually we still use it for bbiab.com .. but we were an early adopter .. when it was still free .. these day you're gonna have to cough up something like sub $10/mth .. still the better deal was in the past...

So what can we use .. we're gonna suggest [Zoho][0]. click the arrow.. there's more to see.. it aint pretty .. but neither was Jaws until you realized it was a flopping piece of crap Hollywood tech ...

---

So lets begin... here are the steps.. follow as tho your Fred Astaire and actually give a crap about what we're showing you ...

..so we start [off at this page][1].. scroll down, past the standard, pro and enterprise pricing, and you'll see free plan. The free plan allows you to use 1 custom domain, and upto 25 users.. now I s'rsly doubt we're going to need more than that.. so click to get started..
![](https://imgflo.herokuapp.com/graph/2b2431f8e7ba7b0/5280d293ead2798e199c9dc735dce7fc/croprotate.png?cropheight=489&cropwidth=860&degrees=0&input=https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fthe-grid-img%2Fp%2Ff9056506484a1c04187fa93f11280e24798540d7.png&x=1&y=0)

The administrator account can be the email you want to use with your new custom domain eg info@muchloveddomain.com

Zoho, will now want you to verify that you own the domain by adding a CNAME record through your DNS. From the last article, we're using Cloudflare to control our DNS, so we would add the record there.

Zoho will provide the name and the alias.. similar to :
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/ba6ad1fd-8f12-42f5-b0bf-c6faa42405f7.png)

Once you have added the record, back in Zoho you can click the Verify button.. now this may take some time... hours in fact.. and you will frequently go back, hit Verify, and it will fail again.. thats the nature of DNS changes.. it's a waiting game..

If it really does seem to be taking longer than say 4 hours.. then Zoho does give other options, such as verifying by a TXT entry. This is what we ended up doing, and allowed us to continue..
![](https://s3-us-west-2.amazonaws.com/the-grid-img/p/8363d5f36217d6602f15cbc09a947a36c117951c.png)

Now that Zoho knows we really own the domain, they'll provide us with the MX records that we need to add to the DNS table. These ensure that any emails to info@myloveddomain.com will be handled by Zoho.
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/a98cf712-3c6e-4c2d-b2ce-304e9fe7bddd.png)

In the Zoho setup wizard, it will also offer some security options, and we followed their suggestion to add SPF, which was simply a case of adding another TXT record into our DNS.

Done! ..we now have a custom domain, SSL provided by Cloudflare, and an inbox provided by Zoho.. well almost done..

It does all work, you just have to login to the web client each time you want to check your mail.. which is a bore.. we need an email client.

Open the Zoho mail webapp, click the gear in the top right to see settings. Under Mail Settings - Email Forwarding and POP/IMAP, you'll find IMAP Access. Change the status to enabled.

We're on a Mac.. if you're not, we'll write an article one day about why you should be.. it has a perfectly good Mail app.. we just need to add a new account using our new email address, and add the imap settings.

The custom domain incoming mail server is imap.zoho.eu and the outgoing mail server is smtp.zoho.com.
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/5b6e4537-0a9b-4ce1-946b-1a81fc7e621d.png)

There.. I promise.. we're finally done... 💤 ..leave a comment below if you have any questions..

<iframe src="https://the-grid.github.io/ed-userhtml/?g=eJxNkTFPwzAQhff8CisImki1nSKxkKRDJIRYOrEhhBz73Lpt7Mq-pC2I_47TphKb7-7Te3fPlTIDMapOdUu9c5guKx5by6QK0psDLjPdW4nG2UzNSZhHNic_CSGD8GQba70NpCaKrQFf9tCBxdCc38V6JTrIQv5RfJaRNppk_5nm_KayKJUTD9h7OzKTkPQgECYuKpRxwIyKM6OuGAtexjLlXDprQSLTQkLr3I5ZQA7267XhQe3YNtyddNvt68XDAD7EI-rhkS2KdNSJi7OD8NFk5RQwYwN4bEA7D9l0WF4mv5lysh9XmZPZNZJZfN0M6TZEo1melxWfAkuqMVK5FyFcUpWuu6SSEiVQ0I0HXacbxEN45ly0kp7O36wPPO6CVEF_okfU1FDlLNKNGIAKS6ETZk-FlK63OCkdjcJNnS6K4n7q2L47uIDR9-n2j3-DUZ9A" height="400" style=""></iframe>



[0]: https://www.zoho.com/
[1]: https://www.zoho.eu/workplace/pricing.html?src=zmail