---
inFeed: true
description: >-
  When you create your new grid site, first you give it a name.. pick a site
  color.. and then you have the option to ‘purchase’ a custom domain name..
dateModified: '2017-09-07T11:58:31.528Z'
datePublished: '2017-09-07T11:58:32.165Z'
title: yes to a name.. yes to ssl..
author: []
publisher: {}
via: {}
hasPage: true
sourcePath: _posts/2017-09-02-yes-to-a-name-yes-to-ssl.md
starred: false
datePublishedOriginal: '2017-09-02T12:10:10.446Z'
url: yes-to-a-name-yes-to-ssl/index.html
_type: Article

---
# yes to a name.. yes to ssl..

When you create your new grid site, first you give it a name.. pick a site color.. and then you have the option to 'purchase' a custom domain name..

For every site you have on the grid you can get a free domain for the first year through their partnership with [Uniregistry][0]. So it seems to make perfect sense to take the opportunity to grab that muchloveddomain.com right now.

If you don't want to do it now, no probs, you can always go back to site settings later and click purchase a domain. The nice part is, Uniregistry are partnered with the grid, so when you obtain your domain, their DNS settings will auto point to the grid, and set it all up for you.

BUT.. is Uniregistry the right place to get your domain.. it's free for the first year, but check the renewal fee for the 2nd year. Depending on the type of domain - .com / .io / .us - it maybe cheaper to go elsewhere..

For [abc-xyz.us][1] we used [Namecheap][2] as the domain provider, as in the long run it worked out cheaper :

* Uniregistry - it maybe a free domain .. but then the yearly renewal is $10.88
* Namecheap - it was only 88 cents... then yearly renewal of $8.48

After the break.. how to set it up so that it points to your grid site, and how to set up SSL through [Cloudflare][3].
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/33b4b5a1-16bc-4fca-9ee0-8d31c8a7896d.jpg)

---

So now that we have our unique domain we can login to our domain providers account, and make the necessary changes.

Within our DNS page, we would need to add 2 A records, one for "@" and one for "www" each pointing to the IP address of Set up two A records. One will be "@" and the other will be "www" both should point to our IP 52.32.215.222

We're not going to do it here though, as we intend to use SSL ie so our website will be http**s**://muchloveddomain.com

We're going to use [Cloudflare][4] for this, as we can do it for free. Once we have signed up at Cloudflare, you will be given 2 nameservers, which we need to use in the DNS settings of our domain provider.. in the case of this website namecheap.

We switched to Customer DNS settings, and added the 2 nameservers provided by Cloudflare..
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/d389ac7d-7b45-4a38-b809-a5dd2d302e7c.png)

Now it's a waiting game.. it can take hours for the change to take effect, until then.. keep building your new site....

🕑 🕒 🕓 ☕️ 🕔 ... ok we're done!
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/b34c56e3-4cb1-4e0b-ace8-4a7652ff5d85.png)

..well not done.. but now we can do the final settings...

Under the cypto tab, set it to Flexible :
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/9a2e6696-c130-4900-adef-7c37e6ad4ae1.png)

Under page rules, create a new rule as in the screenshot :
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/4853ed81-1526-4ca6-a5ba-761c9cac65c5.png)

Your page rule would look like http://\*muchloveddomain.com/\* - Always Use HTTPS

Under the DNS tab, the important part as we first mentioned. Creating the 2 A records "@" (root domain) and "www" to point to IP address 52.32.215.222
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/c1cf09ce-98e2-47c7-a7c8-b4d37433bd8f.png)

You can see the "www" entry at the bottom, the "@" record is shown at the top. We created it with "@", Cloudflare converts it to abc-xyz.us in the screenshot.

The other entries.. css / forms / gallery ..they are just subdomains.. ie https://forms.abc-xyz.us ..but more about subdomains later..

On your grid site, go to Site Settings, top left.. and change the url to your new domain..
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/2bec20de-13db-4229-93a5-f65429d5a36c.png)

For now... we're done! ..see your new website - assuming you were working on it whilst waiting for Cloudflare - at https://muchloveddomain.com

\*don't click the link.. it doesn't really exist.. 4️⃣0️⃣4️⃣

leave a comment if you have questions..

<iframe src="https://the-grid.github.io/ed-userhtml/?g=eJxNUUFOwzAQvOcVVhA0kRo7ReJCkh4iIcSlJ24IIddet04TO_I6oQHxd5ySStw8u-OZ3dlS6pFoWcVqnzlrfbwtWShtoxKF073fJmowwmtrErkmuA7clHxHhIzckSZg1SCpiKQH8E8tdGA81tMrP-x4Bwmmb_l7EdhakeQ_p55eZBKkUuLAD87MnEVIOOAeFl5QKEKDahl6Wv7RKDoRYMyYsMaA8FRxAXtrT9SAZ2A-nmuG8kQbvDmrfddWm7sRHIYlqvGebvJ41gmD0567YLKzEqg2CM7XoKyDZFksLaKfRFoxzKOsyeovklV4XQ2zBoPRKk2Lki2BReUcqWg54iVVYbtLKjGR3PPs6EBV8dH7Hh8Z43uRnacvOiCbADNvM56ZkFy2IMR2-feppT9W8SbPb5eKGbreog8uD9er_QJPmJhe" height="400" style=""></iframe>



[0]: https://uniregistry.com/
[1]: https://abc-xyz.us/
[2]: https://www.namecheap.com/
[3]: https://www.cloudflare.net/
[4]: https://cloudflare.net/