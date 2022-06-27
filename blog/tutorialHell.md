---
title: Rescue from the infamous tutorial hell
date: 05-14-2022
---

### Introduction

As long as you keep learning, tutorial hell will keep following you. Trust me, my journey into the world of programming started 5 years ago in 2017, and continues to this day. It started with FreeCodeCamp, and shortly after that, I fell into the infamous tutorial hell, because I thought I didn't know enough to tackle FCC projects. So I kept following a tutorial after tutorial, written or recorded, did not matter to me. That time I spent copying someone else's code without any critical thinking or asking questions was spent productively, I thought. After a few months, I had nothing to show for my learning, because all I had were projects built by someone on Youtube far more knowledgeable than myself. 

### Endless cycle of hell

You can probably guess what happened next. Yes, I got discouraged and took a pause. This cycle went on for a few years. In that time, I actually did learn a few things: I picked up Python, I knew bits and pieces of CSS, and some algorithms that I managed to solve in JavaScript. I didn't know what I could do with bits and pieces of separate technology though. A lot of times I felt like I was trying to break through a wall while drowning at the same time. Surely, not a great mental space to be in. I knew the big buzzwords like *front-end frameworks, API, and databases* yet it all seemed so unachievable to me. At some point, I even sat down to follow a Ruby on Rails tutorial and got so overwhelmed with all the scaffolded code that I quit not even halfway. 

### The come up

Soon after in 2019, I joined an online learning program called Code the Dream. It gave me consistency, accountability, and most importantly community. After 9 months in that program, I felt like I had not only technical knowledge but an understanding of the overarching web development concepts. Of course, looking back I realize I knew barely anything. I learned Ruby on Rails and made my book-tracking web app with no front-end framework yet. It took me 2 weeks but it was the most satisfying thing I felt at the project demo at the end of the program. 

This year I started my second job as a software developer. Now I can offer some insights on what I could have done things better or differently. But one thing that probably follows me to this day is the tutorial hell. In programming, you never stop learning, which means tutorial hell is always lurking nearby. Perhaps, this is not a secret to some people but I had to discover it on my own through some painful obstacles. Here is what I learned: (it's brilliant and simple actually!) once you finish a tutorial on any subject, do not jump to the next topic, or the next video. Stay on that project and think of ways to add or improve that project. Easy, right? Let's break it down!

### My solution

Recently I started a new job that uses Flask for the back-end. I've used Flask before, but I still wanted to brush up because I felt like I was floating through the codebase. I skimmed through the official Flask documentation, read some blogs, etc. It didn't feel enough. So I gave in and decided to follow a video tutorial on LinkedIn Learning. I like Bruce Van Horn on LinkedIn Learning and he had an interesting [course](https://www.linkedin.com/learning/building-restful-apis-with-flask/making-a-super-simple-api-example-3?autoplay=true&resume=false&u=39411940) on building Planetary APIs with Flask. After finishing the tutorial, I came back to look at it, only to realize that I didn't retain half of the course material. I am a junior developer still mired in coding newbie challenges?! That's okay, learning is not linear. I decided to build a Vue.js front end for this project to not only solidify my knowledge of Flask but also really extend it. Let's break it down!

### Everything is in the details

There's no limit on what features you can add to the app once you have your API endpoints, in addition to refining styling. I only utilized 3 different API endpoints. First of all, let's use a ```
GET
``` request to show all the planets. Here's a ```GET``` API endpoint from my Flask app.

```
http://localhost:5000/planets
```
Here is the list of all the planets. I used some CSS to add basic styling.

![all planets.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652568265136/1ztbwVkbx.png align="left")

To get the information about the planets I used Axios. As you can see, I haven't worked on handling the errors yet. 

![get all planets axios.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652568457245/IreaAIIkF.png align="left")


To show the details of each planet, I used dynamic routing. 

![planet details route.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652568566860/6ch7jcWqy.png align="left")

As you click on each card that contains a planet, route.params.id will be assigned the id of the planet that was clicked on. Next, we will pass route.params.id to the Axios call.

![planet details and route params.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652568966923/Irx6Do2U1.png align="left")

So now we are rerouted to the Planet Details page that looks like this:

![planet details.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652569010698/ZrTepi0sg.png align="left")
Lastly, I have a form that lets the user add a new planet.

![add planet form.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652569173040/Dpdn_EIVI.png align="left")

Adding a new object is also quite easy. First, create the object and assign the input values to the object property.

![create new object.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652569314718/fI8I2VQ64.png align="left")

Then pass it down with Axios call to the Flask app.

![adding an object with Axios.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652569252833/1nYapVT38.png align="left")

### What can we take away from this?

As you can see from my example project, your project does not need to be entirely complete or polished. At this stage, it's all about getting your functionality working. There is an endless number of features I can think of that will make my app even better. But at this stage, it's all about reinforcing what you learn and perhaps learning a few new things too. I can also add new models, schemas, and endpoints in my Flask app so I can make my front end even more engaging. Every new feature you add, will make you research and learn new technology or skills. That way, you are no longer blindly following a tutorial after tutorial. Your learning is based on what you need for a specific feature that your project requires. Using your newly learned skills and building out real features will solidify your knowledge. You don't have to build a whole front end for a backend-based tutorial. Your goals can be on a smaller or a bigger scale, depending on your level of proficiency. For now, find an old project you have worked on by following a tutorial and add a small feature; even if it means making a small CSS change to start.

