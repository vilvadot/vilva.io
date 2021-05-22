---
title: "How to define your MVP"
permalink: blog/how-to-define-your-mvp/
date: '2019-06-05'
tags: [product-building]
---
![How to define your MVP](/images/2019/05/mvp-graph-1.jpg)

The problem
-----------

I had decided my first experiment ([ByteVitae](https://blog.vilva.io/experiment-1-bytevitae/))!

Ideas started flowing like rivers. Every waking minute a ton of features and ideas rushed to mind and I had to note them down. It was going to be the perfect product!! 🙌🏻.  But...here came the first dilemma every product builder has to face: **Where do I start?**

All my previous startup years taught me that ping pong tables are a must for any office and that I had to start with  the barest essential MVP I could think of. Easy! ...right?

![](https://media.giphy.com/media/lELRD773cY7Sg/giphy.gif)

_\*I could (should) have done a validation MVP. For example: Creating a landing page and delivering manually designed CVs and the like. But I purposely skipped that phase and focuses on building a coded product from the start. Shame on me._

Where to start?
---------------

With this in mind, I ran to find anyone around who could help me further develop my idea. And luckily for me, being in an environment like "La Cova" makes sure you are constantly surrounded by experts in some area or another.

Including product people...😈. So I harassed them a bit and eventually, we got together to define my MVP.

Note that I could have decided a few features by myself and start building straight away but remember that **my journey is as much about honing my personal skills as creating products**. And I really wanted to learn how to do product management like the pros. I had done PM in the pat and let's say...the experience was far from ideal.

Makoto to the rescue!
---------------------

![makoto squad logo](/images/2019/05/cropped-Makoto-dot-2.jpg)

I had the immense luck of working with [Makoto Squad](http://www.makotosquad.com/) while building a product during my RUN at [Devscola](http://www.devscola.org/). They made the product development look **organic and surprisingly blockage free**, and in the end, it really showed in the quality of both the product and especially the development experience. Way far from my own past experience where everything was a **cocktail of chaos, incorrect estimations, stress, and occasional shame**.

They were kind enough to hook me up into some of their workshops to learn Product Mapping and User Story Creation and we were ready to start.

> ⚠️ **Shameless promotion**: If you are part or in charge of a product team and you want to improve your process and techniques consider hiring [these guys](http://www.makotosquad.com/). Or at least try to attend one of their workshops.

_\*I have 0 bullshit tolerance in this blog. If I didn’t like them I wouldn’t recommend them,  it's a small thing I do to try to pay them for the invaluable help they gave me for free 🖤. Hopefully, this post gets viral and their site crashes 🙏🏻_

* * *

The methodology
===============

Metho… what? In the past my way of defining a project included these steps:

1.  **Decide a few features I consider are important**
2.  **Code**

Sounds familiar? 🙄 Its a pretty common “methodology” techies tend to use because we **CAN'T WAIT to start coding.**

Well, not surprisingly its **much easier and the result much better if you follow a “real” methodology**. I'm going to try to explain very simply and in my words the process we went through. I'm in no doubt that this must be more formally explained somewhere but I have no clue where 🤷🏻‍♂️. Let's hope you can learn from my experience.

1\. The pitch
=============

We gathered a group of 5-6 people and gave them my short ByteVitae pitch:

*   A **tool for developers** to create and keep an up to date, great looking CV in a fast and easy way.
*   You can **link 3rd party services** to gather information
*   You can **export it to PDF**

* * *

2\. Gather ideas
================

With an image of what your product aims to be, everyone including yourself has a few minutes to write down features/qualities of the product in post-its. Anything is valid here.

![](/images/2019/05/items.jpg)

We got a few more out of frame.

> _**Fast** - **Github Import** -_ _**Export to HTML** - **If I pay I get my info online** - **Manual info** - **Downloadable - etc...**_

The cool thing about this process is that by involving other people you get fresh stuff. **You tend to be too dependent and biased by the idea in your mind**. So, you can get real gems out of this process just by involving someone else.

3\. Group items
===============

With all the items laid on the table, the next phase was grouping the related items together. Basically, stack post-it notes together.

This will make the core areas of your product shine to light, in ByteVitae's case:

*   **APIs**: 3rd party info providers
*   **Export:** How is the generated CV going to be exported/given to the user?
*   **Security/Authentication:** What kind of auth is the product going to implement
*   **Payment:** Payment services, models, etc.
*   **Data gathering:** Is the user going to input data manually, obtain it from a 3rd party’s API...
*   **User Types:** User/Subscription tiers
*   **Templates:** What kind of templates will the users be able to choose from?
*   **Devices:** Where is your app going to run? Web? Mobile? TVs? IE6 🤭?
*   **Language:** Internationalization

As you can see many of these are common to different product-building, see: Auth, Payment, User Types, Devices, and Language **are common to many SaaS products**. But for me, the coolest ones are the rest**, they tend to define where your value proposal is**.

4\. The MVP graph
=================

The next step was to take all that info a plot it into a graph.

The **functionality areas will be the axes of a spider web chart** (no clue the technical term for this) and the **post-it items will make the different steps** on each axis progress/complexity.

This is where the process shines again since it makes you stop to think and order incrementally your items in terms of complexity/cost of development. Also, **it's natural that many more items will spontaneously appear and fill in missing gaps,** giving you a more complete image of the product.

BTW we did all of this with a marker and paper, just took the time to clean it afterward to hang it on my wall.

![](/images/2019/05/MVP_DevCV.jpg)

\*\* Update: 7 October 2019\*\*
-------------------------------

I made a little generator as a proof of concept to create this graphs. You can use it here:

[https://mvp-weaver.vilva.io/](https://mvp-weaver.vilva.io/)

* * *

With everything plotted out its a matter of going axis by axis and deciding where you want to commit. The idea is choosing to **take the axis to the simplest step possible where it gives value to the user**. Thus defining the simplest MVP possible.

Once you have decided each step, join the points and voila! **the area inside your shape is your MVP**!

I LOVED this technique. Having this at hand gives you a really good picture of the scope of your project. Once you have developed your MVP, it will be a matter of growing that shape, the cool thing is you always have a clear picture of where the focus of the product is being made/neglected.

5\. Time to get SMART
=====================

Besides the MVP graph, we needed a definition to keep ourselves in check.  So no better way than defining it with [S.M.A.R.T criteria](https://en.wikipedia.org/wiki/SMART_criteria), so that we are sure the MVP follows our expected rules and we didn't miss anything or got something wrong. If the MVP doesn't fulfill these criteria it isn't finished.

**SPECIFIC**

> We have a web product in english. A user can generate a CV, introducing manually his/her data and extracting it from Github. Chooses a basic template or pays for a premium design. Then can export it as PDF.

**MEASURABLE**

*   A user can download his/her CV with info from Github
*   A user can include manual info in his CV
*   A user uses a basic template for his CV
*   A user can export his/her CV as PDF

**ATTAINABLE**

*   I see it attainable.
*   The highest risk resides in the connection with Github
*   The second risk is my lack of experience in backend development

_\*This made very clear where to focus the initial development/investigation phase_

**RELEVANT**

*   People will pay for a better design
*   Automatic integration of 3rd party info gives value to the user
*   Validates that I am capable of developing the integration

**TIMEBOXED**

*   4 weeks for development
*   1 week for monetization

6\. The product map
===================

![](/images/2019/06/tagged.png)

[Click here to see ByteVitae's full product map](https://app.cardboardit.com/maps/guests/72e19e62b62798f20a75bb4ad40d5189c5ca19b17f905e28da13749d7e9ad2d4)

The result of all of this is the product map. It is an "alive" board that evolves as your product does. Like the MVP graph, it gives you a big _picture_ of the product. Also, **it ties together Marketing, Business and Developing,** and its extremely useful for defining user stories for developing.

Conclusion
----------

*   Could I have defined my MVP without this process? **Sure**.
*   Would I have such a clear picture of the scope of the project? **Nope**
*   Would I have such a rich pool of features/ideas to further grow the product? **Nein**
*   Would I have evolved my product defining skills? **Definitely not**
*   Would I have a cool ass looking spider graph on my wall now? **Probably not**
*   Was it worth the handful of hours we invested in the process? **A big YES!** 🤟🏻
