---
layout: post
title:      "**Error, Error, Go Away!**"
date:       2018-02-14 17:01:25 +0000
permalink:  error_error_go_away
---


I’ve just completed the Intro to Ruby Development section of the Flatiron Full Stack Web Development course.  During this section, we worked on learning Ruby fundamentals and applied those fundamentals by building a TicTacToe game. The process was challenging at times but overall rewarding. 

One of the most problematic topics for me were the nested arrays. The material seemed straightforward but in practice, it became more confusing. TicTacToe game status and TicTacToe in ruby were the two most difficult labs for me to complete and together took at least 3 hours. 

Specifically, I struggled with accessing the correct information in the arrays within my methods. The error messages proved to be one of the most useful tools when solving my problems. I was able to solve most of the issues by reading the error messages and working back through my code to identify the problem. 

During the Intro to Ruby Development section, we were educated on the Single Responsibility Principle. This principle states that each method should have only one function. Previously, during my Flatiron boot camp prep, I was under the impression that grouping an entire solution into one method made the code less confusing. When in fact, it’s the opposite. 

It seemed to me that with everything in one place it would be much easier to read and understand for myself and anyone I was working with. However, compartmentalizing methods and restricting their function to a sole process helps to create more flexible code by allowing the programmer to dive into deeper levels of abstraction and break a problem down into its base components. It was said best in the Flatiron Tic Tac Toe Current Player lab documentation: “Breaking down the behavior of our program into its smallest possible constituents gives us the flexibility we need to take those building blocks and arrange them into new configurations as new goals and problems arrive”.

Learning about the importance of this Single Responsibility Principle not only changed my perspective on the most efficient way to code but it also helped me problem solve in my OO TicTacToe lab. This was my first time using object-oriented Ruby and I was struggling with how to get everything to work together properly. There were over 40 error messages and after reviewing them all I realized that if I was able to make each piece of the puzzle work independently eventually they would fit together. I used this strategy to get my methods to pass individually and I was down to the last few errors. Something was wrong with my play method. I tried multiple different solutions and still, I received errors. I was running out of ideas and the error messages were becoming frustrating. 

At one point I was tempted to change the turn method but while contemplating this I realized that the turn method had no errors. After that realization, I was able to narrow the problem down to the play method; I was missing something. I needed a way to repeat the turn method without modifying the turn method itself. I reviewed the lecture material and realized that I had to use an until loop to call on the turn method within the play method. This would allow the game to continuously take turns UNTIL the game was complete and prevented the player from being sucked into the dreaded infinite loop.  

