---
layout: master
title: Using a Custom Domain
---

Custom domains let you share your files with a URL like `example.com/a1b2`. This
can be tricky to set up and is only recommended for advanced users. If you're
uncomfortable with any of the instructions ask a friend who's done this before
or get in touch with your the company you used to register your domain.

First, you'll need to buy a domain. This usually costs $10-$40 per year. Then
you'll need to follow the registrar's instructions to point the domain to our
servers.

For a sub-domain like `www.example.com` or `cloud.example.com` you need to
create a **CNAME** record and point it to:

    proxy.cld.me

We don't recommend using a top-level domain like `example.com` (no sub-domain)
but rather redirecting all requests from the top-level domain to a subdomain
(e.g., `example.com` redirects to `www.example.com`). Your registrar or DNS
provider can help you with this.

Should you absolutely want to set up a top-level domain (again, we don't
recommend it), you must use **A records** pointing them to the following three
IPs:

    75.101.163.44
    75.101.145.87
    174.129.212.2

Once you have your domain configured using either a **CNAME** or **A record**,
you may need to wait up to 48 hours for the change to take effect. If the domain
is set up properly, you will see the following message when opening it in a
browser:

    Heroku | No such app

If you have verified that your domain is configured properly you can visit
[your account page][account] and enter your custom domain (e.g., `example.com`
or `cloud.example.com`). Click _Update_. If everything went right your links
will now use your custom domain. Try a few and make sure everything's setup
correctly.

Should you want to return to using the CloudApp URL (cl.ly) simply remove your
custom domain from your account page and click _Update_.

[account]: http://my.cl.ly/account
