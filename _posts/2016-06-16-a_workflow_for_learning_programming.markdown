---
layout: post
title:  "A workflow for learning programming"
date:   2016-06-16 18:08:33 +0000
---

## Part 1: Dealing with Confusion and Organizing Knowledge


Learning a programming language is no easy task. In this post, I will begin to layout a workflow that will create some order among the chaos of new vocabulary and underlying concepts. The ultimate goals are to: a) understand a topic, b) set up a review system, and c) create a reference for yourself.

The tools that I use are: a mind mapping program, such as iThought or mindnode, a spaced repetition review program (such as Anki), and finally any text editor. I’ll get into the spaced review system in the next post. For now, I want to talk about dealing with confusion. I will use a few examples from Ruby, but the general idea should apply to any programming language. 

A successful workflow must have self-reflection built in. In this context, I’m using “self-reflection” to mean reflecting on what you do and do not know, and reflecting on how you learn best. Self-reflection doesn’t always come naturally. If faced with a problem, our first instinct is to try and solve it, not to sit back and reflect on what we do and do not know. Also, you can’t really reflect on what you don’t understand until you reach the limits of your understanding. I’ve found that gaining proficiency with an aspect of a programming language involves several steps. In step 1, self-reflection can pay dividends.

Step 1: Confusion
> How do I solve this? 
> This doesn’t make sense? 
> This should work, but it doesn’t, and I don’t know why!

Step 1 is not always fun, but it’s unavoidable. You can save yourself a lot of time by getting an accurate sense of what you *do *understand and what you *do not* understand. This may sound obvious, but it is more difficult than it seems. Take the following example: what does it mean to “iterate over an array?” It is easy to think: “This means to take each element of an array and do something to each one.” But understanding the basic concept is quite different from being able to apply it in different situations, with different goals, different limitations, and using different methods. It's important to bridge this gap. 

The danger of Step 1 is frustration. When you’re frustrated, you feel like you understand what you need to do, it’s just not working. But you understand it, so it *should work*. It’s easy to waste time spinning your wheels in frustration, trying random things without really understanding why they might or might not work. When you find yourself in the confusion mode, it helps to step back—sometimes literally, as in step away from your computer—and try the following exercise.

Take a piece of paper (or if you’re still on your computer, open a text editor) and write or type on the top of the page the subject you are confused about. Then set a timer for 5 minutes and write everything you know about the subject. If you’re working on a specific problem, write in as clear English as you can what needs to happen to solve the problem. It also helps to generalize. For example, say you are trying to figure out how to swap elements within an array. At the top of your page, you can write “Arrays.” Then write the different ways you know how to create an array. Then list all the array methods you can think of, and write a brief description of what they do. When you can’t think of anything else to write, you are done. The important thing is to write everything you know. Don’t worry if you can’t clearly define a method. Say you remember the #any? method, but you don’t remember what it returns. Write `#any?` — tests if any elements of an array are == to x, and returns ??. Things like this are key, as they show you the limits of your understanding. Here it can be helpful to have a marker for things you want to look up later. (Random tip I learned from soneone: if you are using a text editor with spellcheck, TK is a good marker, since there are few English words with this combination. So you can run spellcheck and it will take you to each item you want to do more research on. It really doesn’t matter, as long as you are consistent and can find these little reminders to yourself later on). 

Next, look over what you wrote and look for themes. For example, if you wrote “Arrays contain elements. Each element has an index.” And further down the page, you wrote “Indexes start at 0, not 1.” Then you wrote, “How to access an element of an array: `array[index]`.” These sentences have something in common: they describe basic traits of the array data type in Ruby. Now, with your mind mapping program (or, if you prefer, a piece of paper), start a Ruby mind map create an “Arrays” subtopic, and a further subtopic of Arrays called “Fundamentals.” Create new subtopics of Fundamentals for the above sentences.

This might seem like a waste of time—after all, you can find this info from [Ruby Docs](http://ruby-doc.org/) in a pre-organized form. But the difference is that this workflow forces you to put a) concepts in your own words, and b) organize concepts in a way that makes intuitive sense to you. Over time, as you add methods and modules to your Ruby mind map, you might find that your organization resembles that of Ruby Docs. But getting there yourself is much more valuable, because every time you open your mind map and to add a new piece of knowledge, you decide where this piece fits within your understanding of the language.

An added bonus is that as you continue this process, you are creating a reference for yourself.

Now back to your problem. Hopefully this process has given you a better idea of what you don’t yet fully understand. Once you have pinpointed these areas, it’s time to do some research. Look back at your markers (ie. ??, TK, or whatever you chose) and do some research. For example, above I wrote part of a definition of the `#any?` method. Now is the time to look it up on Ruby Docs, find some examples of it being used, and open your irb and experiment. When you are done studying for the day, go back to your sheet of paper or text document and complete the definition in your own words. Then add it to your mind map.  

Hopefully this workflow helps you deal with Step 1: confusion, avoid spinning your wheels, and gets you started creating your own reference for the language of your choice. In future posts I’ll look at future steps, and how to add an automated review system to your workflow. 
