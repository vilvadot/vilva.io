---
title: "Week #1 - Islands, Auth and Lies"
permalink: blog/week-1-auth-islands-and-lies/
date: '2019-05-17'
tags: [product-building]
---
![Week #1 - Islands, Auth and Lies](/images/2019/05/Island.jpg)

Ok, so I have discovered Im pretty fucking bad at keeping a blog. A lot of ideas spin up in my mind for articles, but I don’t have the built habit of sitting to write them down. Hopefully with weekly updates I can develop it. **🤞🏻**

Also Im pretty much starting with a lie, since its not really week 1, but I need to start the posts somewhere and its my blog so…

The stats
=========

💌 Subscribers to vilva.io…………………7 (all friends)  
💸 Revenue………………………....…………0€  
📝 Articles written…………………………..4 (+1 with this)

![](/images/2019/05/stats-1.png)

I have been tracking my time with [Toggl](https://toggl.com/). Take the numbers with a pinch of salt, because I tend to forget A LOT, to activate the goddamn thing. But I believe the relative time allocations are ok.

TL;DR
=====

*   Im a shitty blogger. Trying desperately to post regularly with this new updates
*   ByteVitae grows, auth done, landings live, GitHub info gotten and PDF generation working
*   Im learning how to test a lot of stuff with Jest!

The last weeks
==============

To put it short the last month or so has been hell on earth logistically speaking: I moved into an island, had to find a home, looking for a car , a place to work from etc… but thankfully most of it is over! And I managed to squeeze some time out for working on my first experiment: [ByteVitae](/experiment-1-bytevitae/)

I wanted it to be already released, but hey, life happens.

ByteVitae
=========

I feel like posting updates on the developing topics Im tackling week to week, since Im finding some seriously good info on them and it would be pretty cool if someone might save the time it took me to figure things out.

The investigation
-----------------

Before building the product I had to validate 2 things first:

*   **I can generate PDFs of great quality**: I was afraid I couldn’t match the quality of a hand crafted CV.  But I did it! And Im extremely pumped with the result. Thanks a bunch to the people behind [React PDF](https://github.com/diegomura/react-pdf)

![](/images/2019/05/CV-zzarcon.jpeg)

(Left generated template, right hand crafted CV of my friend from a few years back. Thank @zzarcon!!)

*   I can get the info I need from Github API: I had never used the GitHub API, but got it to work in a few mins and got all the info I needed! Easy peasy with the official [GraphQL lib](https://github.com/octokit/octokit.graphql.net)[r](https://github.com/octokit/octokit.graphql.net)ary

More progress:
--------------

*   **I swaped [NextJS](https://github.com/zeit/next.js) for [Create React App](https://github.com/facebook/create-react-app) in the front**: This was a big one for me since I love NEXT but I started to run into some problems with the PDF generation and Server Side Rendering. Decided to ditch it before I lost more time trying to hack it to work. Cool thing is that the project seems to be well architected, it took 10mins to swap them!
*   **Made a kickass landing page**. And deployed it with [Netlify](https://www.netlify.com/) ❤️

![](/images/2019/05/ByteVitae_mockup-2.png)

*   **DNS and domain Setup**: [bytevitae.com](http://bytevitae.com) is live! The product will live under dev.bytevitae.com or something along those lines.
*   Managed to **keep most of the code tested** learning a ton about Jest mocking in the way (expect some articles about this soon)
*   Learned way more about **setting up SSL certificates with NGINX** than I wanted 👍🏻

Authorization
-------------

This item deserves its own section. It took waaaay more time and effort than expected. “Everyone does authorization it must be really easy to implement right?….right? 😥”

I had never done this kind of work on the backend. And oh god I have a new gained respect for my former backies. The thing is that implementing it in the API was not difficult at all. But understanding the correct OAuth flow was a pretty decent challenge for me.

*   **Used Passport.js:** This gives me a ton of stuff out of the box like endpoint protection, and leaves the door open to implement multiple login systems in the future. Couldn’t have done it without this:

[OAuth (Passport.js) Tutorial #16 - Cookie Session - YouTube](https://www.youtube.com/watch?v=5dQsR9Kcnzc&list=PL4cUxeGkcC9jdm7QX143aMLAqyM-jTZ2x&index=16)  

[node.js - Understanding passport serialize deserialize - Stack Overflow](https://stackoverflow.com/questions/27637609/understanding-passport-serialize-deserialize)  

*   **Persist session** using experss-session, mongodb as storage and cookies:  

[Fetch API with Cookie - Stack Overflow](https://stackoverflow.com/questions/34558264/fetch-api-with-cookie)  

*   **Protected routes** in the frontend with ReactRouter:

[Protected routes and authentication with React Router v4](https://tylermcginnis.com/react-router-protected-routes-authentication/)  

![](/images/2019/05/simple_browser_mockup.jpg)

A few weeks work... 👀

Next steps
==========

*   Capture the emails from the landing (using Mailchimp?)
*   Launch the landing page and get some feedback!
*   Since the authorization workflow is generic I plan on including it in a product scaffolding and releasing it public.
*   Next generic piece is payment workflow, so working on that next
*   Build the PDF generation workflow
*   I should really try to do some marketing before releasing 😅

Expected release
================

The product is advancing at a pretty decent pace, wanted to release it on the 22nd, but life has taught me that my estimations are… imprecise. Some real life is getting in the way the next week, so **I will aim to launch around the 10th of June**.

Vilva.