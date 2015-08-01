---
layout: post
title: Creating Composed Game Entities
categories: []
tags: []
published: True
date: 2015-07-31 17:20:34
---

I think I may have gone off the deep end a bit, I promised I would keep things simple and not care about being correct but of course I failed at that like I always do.

So I misunderstood the basics of composition based game entities and I tried making a convulted generic reusable completely inheritless system which made no sense. I had to step back again and take a breather while looking at what I wanted to achieve, and maybe understand why my initial goals were not correct rather than my failed implementation. 

So what did I want to achieve?

* Use "components"
* Avoid inheritance
* Magic

So looking at those points and what is wrong with them.

### Use "components"

I put components in quotes because I guess I really didn't have a clue what composition was. I was thinking along the lines of generic components that did specific stuff. However I really started to get hung up on the implementation details and the generic specifics. I was thinking in terms of a simple array of Components and really started down a rabbit hole.

What I basically said was I wanted to work with the composition pattern for writing games but I did want to do it fast and dirty but then I tried to come up with a generic beautiful reusable example which I have to stop trying to do when I'm trying to hack, I have an instinctive habit to make things clean robust and professional all the time but that just gets in the way and causes too much theorizing when I really should just be solving problems.

### Avoid inheritance

Okay so I read on the internet that inheritance is bad and I jumped all over that and decided to never inherit from anything ever. To be fair I spend all day working in Clojure which has no classes or inheritance anyways so I figured that would be easy. Well like all zealotry, going from one extreme to the other results in a different but still equally bad design. When the internet says "inheritance is bad" what they are saying is "large complex inheritance heirarchies are bad" which is what I am trying to solve by using the composition model. However trying to get away with absolutely zero inheritance in C++ is not exactly what I am looking for either. Inheritance is still great at reducing code duplication and good at providing scope, two things that even though heavy inheritance is bad, light inheritance is good.

So in short, now I am going to allow inheritance, because not doing so is stupid. My bad.

### Magic

This one is a little on me and again deals with my inability to write poor code even if I am trying to write poor code in the first place. This isn't some cheezy line in an interview where someone asks what is a weakness I have and I tell them about my inability to not write flawless code, because let's be honest, my code is probably pretty flawful (not a word I know) but I don't want it to be. I read a lot about developers and their rapid prototyping phase or their get things done to test something out steps. I never seem to be able to do those, I always over analyse and spend time thinking about how to do it right rather than just doing it and I never end up getting it done, right or wrong.

So I am off to write single level inheritance (might be more if I *really* need it) and I am going to compose behaviours in the entities via hard coded member attributes! Take that sensibilities!
