---
title: 'Microsoft and the oddities of accepting emails'
taxonomy:
    category:
        - news
    tag:
        - server
        - microsoft
        - email
        - blacklist
aura:
    author: dan
media_order: 'microsoft-outlook-office_365-undelivered_mail .png'
---

# Microsoft and the oddities of accepting emails

Microsoft has had some problems with its Exchange services this year - https://blog.mxtoolbox.com/2022/01/. Maybe it has nothing to do with the problem of one of our customers, but Microsoft has very strange methods when it comes to accepting emails. 

In this particular bug, mxtoolbox mentions that some emails may not even reach the destination. So don't be surprised if you send photos to your family and friends or an invoice to your client and don't get a response back. It could be exactly the reason that they did not receive your email.


## Microsoft randomly blocks IPs

In our case, our customer was simply banned without any reason. The server is running over years and after some tests, nothing strange behaviour happened before or after.  
Microsoft is known for randomly blocking IPs or generally using weird techniques when it comes to emails. Hetzner, Digitalocean, Linode, mailbox.org, protonmail.com ... they all have ongoing problems with Microsoft. And no one can really say why Microsoft keeps blocking IPs.

Not even Microsoft itself knows it:

> Hello,
>
> My name is "THE NAME" and I work with the Outlook.com Sender Support Team.
>
> I do not see anything offhand with IP: (OUR CUSTOMERS-IP) that would be preventing your mail from reaching our customers. 


Another email:

> We were unable to identify anything on our side that would prevent your mail from reaching Outlook.com customers.
>
> If you are still experiencing deliverability issues, please reply to this email with a detailed description of the problem you are having, including specific error messages, and an agent will contact you.

So we responded directly, and it's pretty obvious that the problem is on Microsofts side:

> host
    css-one-microsoft-com.mail.protection.outlook.com[40.93.207.0] said: 550
    5.7.511 Access denied, banned sender[IP]. To request removal
    from this list please forward this message to
    delist@messaging.microsoft.com. For more information please go to
    http://go.microsoft.com/fwlink/?LinkId=526653. AS(1410)
    [CB1PEPF0000205E.namprd00.prod.outlook.com] (in reply to RCPT TO command)

But it seems that mainly 365/Outlook business users are affected. Home users with Outlook or Hotmail accounts seem to work fine. At least we tried our private test accounts (outlook & hotmail) and there are no problems.  


# Microsoft has his own RBL (Realtime Blackhole List)

It would be great for everyone if Microsoft would also use the RBL lists that have been freely available for 25 years. But unfortunately this is not the case. Microsoft uses its own list.  
Checks for us and other email providers leaves us in the dark. 


# Microsoft delisting requests

There are a couple of options you can try:

- https://sender.office.com/
- https://support.microsoft.com/en-us/supportrequestform/8ad563e3-288e-2a61-8122-3ba03d6b8d75

In our particular case, there is nothing we can do. We can only annoy them and send them more emails to finally delete the blocked IP.   
If you have other ideas, let us know in the comments below or at [fosstodon](https://fosstodon.org/@techsaviours).