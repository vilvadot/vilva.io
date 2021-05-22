---
title: "Choosing a Tech Stack"
permalink: blog/choosing-a-tech-stack/
date: '2019-04-03'
tags: [product-building]
---
![Choosing a Tech Stack](/images/2019/04/header.jpg)

Things have been shaping up great during the past few weeks. I have been tying up loose ends on my plan and harassing all my expert friends to gather their opinions, ideas and any useful info I could get my hands on.

(Thanks to everyone who suffered the harassment 🖤)

The journey is starting a bit slower than expected buy I have been working on quite a few things. One of them is setting up a project scaffolding I can maintain and reuse to start product-building in “the most efficient way possible”.

TL;DR
-----

*   Javascript as the language
*   Express in the back-end
*   React in the front-end
*   Everything dockerized and deployed to Heroku

😼👉🏻 [https://github.com/vilvadot/experiment-scaffolding/](https://github.com/vilvadot/experiment-scaffolding/)

Why?
====

Why should I do this you may ask. Why don’t you start writing code for your real project and start producing value from day 0?

It’s a very valid concern, but I decided to do it this way for a few very personal reasons:

*   _I HATE starting product-building_: I really dislike the phase of setting everything up, it can be somewhat satisfying (specially thinking about the architecture) but setting up all the initial pieces and make them work together (specially in the front-end!) feels very boring and tedious to me.
*   _Im not going to focus ONLY in production_: I have decided (thanks to some very good friends advice) to take this journey as an experiment and a learning experience, and diverge a bit of my initial focus on 100% just money generation.  As a result of this, I took way more time than necessary in building this, understanding it and trying to learn the most from those I had access to.

I could have jumped straight into building my first project with my actual knowledge. But as a friend told me: _The real value on this experiments you are going to work on, is your personal growth. Thats, what is a truly valuable asset. A monthly revenue is fragile, but a solid skill base is exploitable until you die._ Wise words.

*   _I believe this will save time on the long term_: I know, I know… this is pure speculation and a really bad thing to do. But I have used this stack for quite some time now, and I believe I can maintain it with minimal effort and will save me time and specially energy when starting a new project. Time will tell.

What language?
--------------

Easy decision: _Javascript_

Im very productive in it. _I can use it both in the front-end and the back-end_. And even though I am way more capable in the former, my experience with the language will aid in my lack of back-end knowledge.

I have been told that Javascript is not the best language for my goals because of the "immaturity" of its ecosystem and the usual scenario where you can do a thing  in 1000 different ways with 131455 different tools. Apparently Ruby on Rails is a delightful experience to build apps fast and efficiently. But since I am used to the Javascript way and I have virtually 0 experience with any other language, I’m quite happy with it.

No better scenario than a total lack of options to get to love your decision 😁.

Architecture
------------

The next key decision is how to structure the applications. Each product will have its own specific needs, but as a template for starts Im using this basic model:

![](/images/2019/04/architecture.jpg)

Every front-end client is a Single Page Application (SPA) that communicates with the back-end via REST API. The server is connected to an external DB hosted somewhere else.

This is a quite common configuration that is extensively used nowadays, also Im very used to it, so the learning curve will be pretty minimal.

This was pretty easy to decide TBH, the interesting part comes when we dig into those adorable coloured boxes. Deciding what to put inside of each one is the fun part.

Front-end
---------

![](/images/2019/04/frontend.jpg)

Ok, this is my area! Im comfortable here, but still the options are great and its a delicate place to be, the front-end side of the internet is evolving at an alarming pace. I have some key problems to solve:

*   _Javascript framework_: The options here are pretty clear: Angular, Polymer, Vue or React. _Im going with React_. I am very comfortable using it and so far the experience has been enjoyable.

From here on I have a bunch of flavours to choose from: Implement a new config from scratch, using a pre-made scaffolding, using Create React App... or what [_Im going with: \[Next.js\]_](https://github.com/zeit/next.js/)). It gives me SSR out of the box, I love the way it handles routing and it has a ton of examples with different integrations.

*   _State management:_ Im going with [_Redux_](https://redux.js.org/basics/usage-with-react) Its integration with React is incredibly well documented, I have used it in the past and I have missed it for 2 years in a previous project (that surely means it must be good right?)
*   _Communication_: For the communication between client an server I have two options in mind: REST API and the fancy new kid on the block GraphQL. /To be honest you already know the answer since I posted a spoiler in the previous section/.

Im going with the _native fetch()_ to connect with a _REST API_. I have used GraphQL in the front-end in the past and liked it. But chances are my Apps are going to remain relatively small and I don't think the benefits of using GraphQL make it worth the complexity it introduces.

*   _Testing_: I will be using some kind of "visual testing" tool like [React Storybook](https://storybook.js.org/) or [Docz](https://www.docz.site/) on the component side. Jest for unit testing. And the amazing Cypress which I have learned to love in the past few weeks to test end to end stuff.
*   _Styling_: This is another tricky place. So many options and opinions on styling React apps. In the past I have had great experiences with [Styled-components](https://www.styled-components.com/) but lately I have been doubting about it. Not sure if it might be better to use _CSS modules_ and keep using BEM named classes for everything to keep it more "React Agnostic". This one is yet to be decided, but for sure it will be one of these two options
*   _UI Library_: I might want to use a UI-library if I want to build interfaces fast.  I  just have yet to decide on using a React component library like _[_Semantic UI React_](https://react.semantic-ui.com/)_, using light css framework like [_Bulma.css_](https://bulma.io/) or even a combination of both. Things will eventually clear out once the project starts to take shape.

All of this will have to be transpiled using [Babel](https://babeljs.io) to use all dem juicy ES6 features and JSX with React.

Back-end
--------

![](/images/2019/04/backend.jpg)

This is where Im nowhere near comfortable. Im familiar with back-end concepts and technology, but I have gotten dirty very little in this area.

I will be using [_Express_](https://expressjs.com/) in the back-end and that is basically everything I know about it. I will try to stick to a Service/Action architecture similar to what I have learnt at [Devscola](http://www.devscola.org/) like the one used in the [Rekaizen Project](https://gitlab.com/devscola/rekaizen_devscola)

I will transpile ES6 with [Babel](https://babeljs.io). Its not as necessary as in the front-end, since Node has way better support of new features than the browsers. But I feel its a good practice to write the same kind of code on both parts of the project.

Also considered Firebase as an option to reduce the boilerplate for most of the CRUD stuff and reduce the back-end surface. Discarded it, since I don't like the idea of having my possibly unique source of income so attached to Google's desires and specific technology. I rather use a more generic approach and technology I can deploy anywhere without having to jump through hoops.

Devops
======

![](/images/2019/04/devops.jpg)

Im no Devops expert. I have a serious lack of experience on managing servers and putting things into production and I want to keep management on this front to a minimum for several reasons:

*   _Time_: By spending some time with my former CTO partner, I know sysadmin stuff can turn into a veeeeeeery time consuming and hair losing endeveaour.
*   _Security_: I know little enough cyber security to know that you can fuck up server stuff in a million different ways, and that it can get pretty nasty when someone who shouldn't discovers it. Also see the previous point, securing your servers is difficult and very time consuming. I rather focus just on writing secure code and leaving the machine management to someone who knows better.
*   _Fuck-up-ability_: See previous point. Besides the obvious possible security fuckups, theres another million ways to fuck things up, not directly related to security. And here is where fuckups get real, with your server down your site is down, everyone is angry and things get intense pretty fast 😅.

As you can see, it is very important for me that the project requires minimal server and DB maintenance.

So with all of this in mind. What I ended up doing is using [Docker](https://www.docker.com)  in both the front-end and the back-end and using a PaaS like Heroku to deploy.

I did some tests and it was a really nice experience! I can release a new version of either of the project services with a single command  without all the overhead of server management. And thanks to Docker the development experience is delightful and if I ever decide to switch providers things will be very easy 😗🤞🏻.

I was tempted on using Serverless functions (Lambdas, Cloud functions etc...) to simplify even further. But the truth is, as cool as they sound I have 0 fucking seconds of experience with the stuff, so its to risky to jump into it from the start. I might try them in the future when Im more comfortable.

For the DB I will use a similar approach and hire another PaaS to take care of it so I can focus in my strength which is developing product, not managing machines.

Now what?
---------

With all of this ready and working, I can start to build my first experiment, but… First, I want to test myself with starting a new project and producing from scratch by using this scaffolding.

So in the following days I will be working on \[Cabify’s Back-end Challenge\]([GitHub - cabify/backend-challenge: Cabify Backend Technical Challenge](https://github.com/cabify/backend-challenge) with a bit of a spin, I will add a DB and a front-end to test the full capabilities of my stack. _And more importantly, my own ones_.

This might sound like a weird decision. Why not start your first project ASAP?… Patience! A good friend of mine, great developer, has offered to review my result in this little practice, and that will help me tons in creating a solid base of knowledge for the first project. Im starting a bit slower than planned initially, but the experience is showing to be worthwhile :D
