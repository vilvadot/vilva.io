---
title: "Week #4 & #5 - Payments, new Illustration and Shame"
permalink: blog/week-4-5-payments-new-illustration-and-shame/
date: '2019-06-18'
tags: [product-building]
---
What do we have here? 2 posts for the price of one? can it be?... of course not.

I'm wearing the shame hat right now, I hoped to stick to the writing streak for a few weeks at least, but it couldn't be. On the plus side, the lack of writing was compensated with a ton of work, both on the product and on Real Life™️

Without further ado, here comes the update.

TL;DR
-----

*   Wrote a post about [How to Define your MVP](/how-to-define-your-mvp/) and its getting posted to IndieHackers
*   Received the finished illustration
*   Integrated Stripe payments
*   Integrated account subscriptions
*   Tested a lot of the product and killed some bugs

The stats
---------

The lack of marketing reflects in the stats, but I wanted to give a good push to the product development this month

**Blog**

📩 Subscribers to vilva.io……………………15 (+0)  
📝 Articles written……………………………..8 (+2)

**ByteVitae**

📩 Subscribers to bytevitae.com…………... 34 (+0)  
📄 Feedback Form answers…………….……34 (+0)  
💸 Revenue………………………….……….....…0€

![](/images/2019/06/week4-5.png)

* * *

🎨 The Illustration is here!
----------------------------

![](/images/2019/06/bye.png)

The illustrator sent me the final result! My experience working with her surpassed by far all of my expectations. I have to note here that she took so much time to finish it because **I expressly asked her to give lower priority to my stuff** and take as much time as needed.

I didn't have an immediate need and I have been in the freelancer position in the past and **it SUCKS to have someone poking you with a stick at every minute**. I rather let those creative juices flow and make their magic. And they did!

I really really really love the result! It's incredible how good she got the idea out of my head, I guess my **sounds and energic hand gestures ARE an effective way to convey designs** (remembering that for the future). I'm sure I will be working with her again, it's not easy to find someone who can mine your mind!

**If you want some top-notch quality illustration I suggest you [check Cou out](https://www.instagram.com/coufeis/).**

How to define your MVP 👉🏻 soon in IndieHackers!
-------------------------------------------------

If you read the blog, you probably saw that I published another post: [How to define your MVP](/how-to-define-your-mvp/)

This post was in the back of my mind practically since I started this journey. One of my goals is building bootstrapped products. The other is leaving material written so people can learn from the process.

**Defining the MVP was a process I particularly enjoyed and where I learned a ton**. So I'm really happy that the post is finally written and even happier because....it's going to be published to [IndieHackers](https://indiehackers.com)!!!

![](https://media.giphy.com/media/RrVzUOXldFe8M/giphy.gif)

I think its a great resource for other fellow indie hackers so I submitted it to the site. And guess what, they approved it! so it will be published sometime in the (near?) future.

I'm curious to see how much traffic that post gets and brings here.

💳 Motherf\*\*\*g Stripe payments following SCA
-----------------------------------------------

![](/images/2019/06/Screenshot-2019-06-18-at-13.10.28.png)

This image is from [Stripe's blog](https://stripe.com/billing-eu)

And in this new episode of Backend Adventures...

Most of the work these weeks have been integrating Stripe payments. To be completely honest now that it's finished it doesn't look as difficult, but getting it to work was a daunting task.

The thing here is that **[a new regulation (SCA](https://stripe.com/docs/strong-customer-authentication)) affecting online payment is going live soon**. This means the client and server have to enter **an undefined loop of communications to complete the authorization** of the payment. Which complicates things a bit more than before.

It was quite confusing but once I got my head wrapped around the process it was a breeze to integrate. Again the quality of **Stripe libraries and the API documentation made things much easier**.

With all the time it took and all I'm extremely happy with the result. This is one of the generic must-have pillars of every SaaS and it's ready!.

💰 Subscriptions
----------------

With payments done the next thing of the list was to set up subscriptions. I wanted to stay away from Stripe subscriptions API right now **not to overcomplicate things and remain flexible**.

I'm not sure of what the final business model is going to be, so I rather implement something generic like single payments and manage the subscriptions myself, which is fairly trivial.

So now users can pay and promote their accounts to "Premium", "Subscribe", etc. which in turn **will open up the gates of some features**.

🐞 Bugs and testing
-------------------

I spent a loooot getting things tested properly and catching little bugs. This is having a great impact on improving my coding skills and **I wanted to have the most I could tested up to this point**.

**Authorization, Payments and Subscriptions are a very important core part of a SaaS** and having this tested properly will certainly improve my quality of sleep in the near future.

I'm still having some trouble implementing End to End (e2e) tests in  the frontend with all this third party services on the way, but I'm working on it!.

📝 Started using Grammarly
--------------------------

So I realized do a lot of grammatical errors. I have started using [https://app.grammarly.com](https://app.grammarly.com) in the hopes of improving my writing skills. So expect less errors in future posts.

It's a shame it doesn't work on Ghost's editor. But hey, you can't have it all.

Next steps
==========

I'm fairly confident I can have a working MVP next week 😱

*   **Implement the PDF printing workflow**
*   **Implement the business model**
*   **Try a closed beta with friends and family**

Another thing I will focus on after the launch is on **releasing the scaffoldig I have developed for this project**, it's highly opinionated but I guess it could help someone shave quite a few hours off of their product-building 😁
