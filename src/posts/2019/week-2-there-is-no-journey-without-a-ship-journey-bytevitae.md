---
title: "Week #2 - There is no journey without a ship!"
permalink: blog/week-2-there-is-no-journey-without-a-ship-journey-bytevitae/
date: '2019-05-24'
tags: [product-building]
---
![Week #2 - There is no journey without a ship!](/images/2019/05/ship.jpg)

Guess who’s back? Two weeks in a row, this is a new record!

[Last week's post](/week-1-auth-islands-and-lies/) has been INCREDIBLY useful to reflect and see where I am focusing/wasting my time. It really served me to realise I had been neglecting the marketing side of the project way too much (oops). To be honest I already knew it, but nothing better than some hard stats to get you out of your bubble!.

So this week I have focused mostly on Marketing and some coding to assist it:

The stats
=========

### Blog

📩 Subscribers to vilva.io……………………15 (+8)  
📝 Articles written……………………………..5 (+1)

### ByteVitae

📩 Subscribers to bytevitae.com…………... 31 (+31!)  
📄 Feedback Form answers…………….……31 (+31!)  
💸 Revenue………………………….…………0€

![](/images/2019/05/Screenshot-2019-05-24-at-10.16.19.png)

TL;DR
=====

*   Handled email account for ByteVitae
*   Connected the landing to capture emails to a Mailchimp list vía Netlify functions ❤️ (I’m in love with Netlify)
*   [Created a Typeform](https://vilva612199.typeform.com/to/qoEbpI) to gather information of how people handle CVs
*   Made a soft launch!!
*   Working on my first outsourced collaboration

📬 Mail capture
---------------

If you remember [last week's post](/week-1-auth-islands-and-lies/), I left a landing finished, but the mail form was not working yet. I didn’t want to save the emails straight to a DB, I wanted to integrate with Mailchimp or other mailing service so that **they take care of handling the list, confirm the subscription etc…**

![](/images/2019/05/Screenshot-2019-05-23-at-17.48.02.png)

I didn’t want this to depend on my main server , and since I have been wanting to try server less functions for quite a while I decided to try [Netlify functions](https://www.netlify.com/docs/functions/). Which turned to be a great idea!

Im delighted with both the development/deployment workflow as well as the result. Im definitely falling in love with Netlify 💒.

They basically built **a layer on top of Amazon Lambdas** so that you don’t have to mess with that extremely sexy and simple AWS panel **\*_irony_\***. It has been a breeze to deploy, and thanks to the ‘[netlify-lambda](https://github.com/netlify/netlify-lambda)’ package a breeze to develop too. _(Netlify should really read this and sponsor me or something)_

This was my first time working with http calls without a framework like Express behind it. And it help me realise **how much I take for granted when working with frameworks**. This exercise took me to a lower level and I had to build the responses manually, which gave me a few problems with CORS (not something new), but where easy enough to fix thanks to this:

*   [Circumventing CORS with Netlify Functions & Nodejs - Glittering Glob of Wisdom](https://glitteringglobofwisdom.com/circumventing-cors-with-netlify-functions-nodejs/)

Overall **it helped me learn more about the http protocol**, so I am pretty happy with it. Oh, and also learnt [how to do Basic authentication](https://stackoverflow.com/questions/43842793/basic-authentication-with-fetch).

Even learnt a few more things about my beloved fetch API. For example, [this thing which I had no clue about](https://stackoverflow.com/questions/38235715/fetch-reject-promise-and-catch-the-error-if-status-is-not-ok):

> Promises only reject with a TypeError when a network error occurs. **Since 4xx and 5xx responses aren’t network errors**, there’s nothing to catch. You’ll need to throw an error yourself to use Promise catch

![](https://media.giphy.com/media/xT0xeJpnrWC4XWblEk/giphy-downsized.gif)

Mail server setup
=================

In other to create a Mailchimp account I needed an email account. So I went forth and signed up at: [Private Email](https://privateemail.com/appsuite/index.html), a simple and usable mail service.  I love to use it to test things out since its dirt cheap.

If the project grows as expected **I will probably migrate to a more robust provider.** But for now this will do the job.

This only involved setting up a few records in my DNS provider and in a few minutes everything was propagated and good to go! So now you can reach me at contact@bytevitae.com!

👨🏻‍💻 How do people handle their CVs?
=======================================

Good question! Until now, all the info I had about this, was pretty much my anecdotal experience. If you know a thing or two about business, it is a **REALLY BAD idea** to base a product on your own assumptions. So I went ahead and [created a Typeform](https://vilva612199.typeform.com/to/qoEbpI) to learn more about others experience.

I wanted to answer the following  questions:

*   **How do people create their CVs right now?**
*   **How often do they update them?**
*   **Are people willing to pay to get a CV done?**

On the other hand I wanted to see if I could capture some leads I could future interview to learn more. And it was quite a success, most of the people who answered subscribed!

Im pretty ashamed to admit it, but I should have done this the very first day I started with ByteVitae. The truth is, **I was to eager to start coding** and little enthusiastic about having to interact with real people 😅 On the plus side I guess that validates me as a good engineer…right? 👀

I will let the form some time to to capture more data and **publish the results next week**. So please fill it in and send it to your friends/coleagues!

[How do you manage your curriculum?](https://vilva612199.typeform.com/to/qoEbpI)

**And thank you so much to everyone who filled it!** ❤️

Preparing the Ship
------------------

With the mail collection sorted out I **wanted to ship something ASAP to keep things rolling**, so I had to do a bunch of minor fixes in the landing to have it ready:

*   Created a favicon
*   Polished the landings responsive so that it worked (kind off) in mobile too
*   Added Google Analytics tracking to the landing (I would like to avoid using Google's products when possible, so if you can suggest any alternative please tell me)
*   Wrote an [About page](http://bytevitae.com/about), to offer some context. I feel like the landing, **still fails to convey what the product is about**, but this will improve soon.

🚀 Shipping!!
-------------

Chan, chan! 🥁. I made my first launch 🎉🎻🎉🎳🎉🤟🏻🚀

Ok, it was a soft launch..but it counts!

I didn’t expect this, but I had a HORRIBLE day, I was waaaay to stressed and nervous about this. One thing is building something comfortably in your room, and another is releasing it into the wild and exposing yourself to judgement specially from your own colleagues!

And here it goes:

![](/images/2019/05/analytics.png)

Exponential growth baby! Those are some pretty shitty numbers TBH, but its exciting to see things start to gain traction!

I kind of piggibacked on top of the form I created to peak people's interest on the product. And it worked since an impressive 79% of people wanted to be noticed once the product is released.

![](/images/2019/05/type.png)

These are mostly people who know me personally, so take this metric with a pinch of salt

As you can see it was a very soft launch but it got things rolling, I sent it just through a few channels:

*   **IndieHackers**: It is a very friendly community, everyone is used to extremely early stage products and Im used to it, so its a safe environment for me. I created a [profile for the product](https://www.indiehackers.com/product/bytevitae), filled it in, and wrote the minimum requirement of 3 posts to have it approved.

![](/images/2019/05/Screenshot-2019-05-23-at-17.51.35.png)

_Mental note: Make a logo that is not shit._

*   **Valencia dev Mattermost (~100 people)** : I got a ton of responses and feedback from here, but again most people here personally know me. Love you guys/gals 😘
*   **Madrid dev Slack (~1.000 people)**: I posted it to a _#random_ channel and got a few answers and some good feedback. Just a handful of people know me here so it wasn't so succesful.
*   **Friends and Family**: Send it personally to a bunch of techie friends, most of them answered and subscribed. Thanks!

And the results:

![](/images/2019/05/typeform.png)

I created English and Spanish versions.

I wanted to take the rust off and jump into the blue, even if close to the coast, and it worked. For the MVP launch I have other channels in mind, but I didn’t want to “burn” them at such an early stage.

So yeah, I had a really shitty day but on hindsight Im extremely happy that I launched, even if it was just a landing page. I got a ton of feedback, a few leads and the most important, I broke the wall that was separating my product from the real world.

🎨 Outsourcing illustration
---------------------------

This may sound silly but it’s a big one for me. I want to learn how to outsource work. Im the type of person who tries to get everything done himself, which is good for what Im doing but **it is not maintainable on the long term**.

So since I want an illustration for the landing, and my illustration days ended a long time ago. Im going to outsource it. Its mainly a test to see how the experience goes,  but I hope to find someone I can build  an ongoing relationship with. Always wanted to have an illustator at hand, since I love it and its something I have never excelled at.

I posted the offer to [PeoplePerHour](https://www.peopleperhour.com/dashboard/seller), a site I used to do freelance work at. Already gotten some promising answers. We will see how it goes.

* * *

Next week
=========

*   Integrate Stripe as a payment method
*   Clean and release the generic product scaffolding
*   Make info on the PDF templates variable
*   Decide on a final business model
*   Work on the PDF printing workflow (probably won’t fit on next week)

On Marketing and community
==========================

This week I realised I'm waaaay out of my comfort zone when It comes to interacting with other people online. I never had to do this in the past, but if I'm going to keep building stuff alone **I better start fucking loving it**.

So I'm going to make a conscious effort from now on, to be more active on the communities I belong to.

![](/images/2019/05/indie-answers.jpg)

Even though it felt scary, at the end it was people just trying to help other people out! (lets see how Hacker News goes… 😬)
