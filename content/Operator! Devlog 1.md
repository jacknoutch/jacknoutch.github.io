---
date: 2025-04-10
tags:
  - blog
---
I enthused with a recent contact over a mutual love of puzzle and mystery games that give a true feeling of deduction. (Among the best are Obra Dinn, The Case of the Golden Idol, Her Story, and Type Help.) We also recently formed a team to compete in this year's CS50 Puzzle Day. Now before our next catch-up we've agreed to make each other a small (!) mystery game.

Chris has sensibly opted for a text-based game. I, on the other hand, have set myself the challenge of making my first game with a graphical interface. The theme is based on a trip to the Museum of Vancouver, where I came across a manual telephone exchange from the interwar period. I was immediately struck with how this could make an excellent game, acting as the operator ("Operator!" - a great name to start off!) connecting callers and - importantly - _listening in_.

I briefly looked into building the game in Java, a language I don't know but one which would be more suitable for a game than Python and the webdev languages I have been used to. But, whilst I would like to learn Java, it looked like it would be too much to grapple with when I want to be able to get a prototype up and running and I had about 5 weeks to make the thing before sharing it with Chris. You can only learn so many new things all at once!

So I've elected to use Pygame, a Python module and wrapper for SDL. Pygame is fairly slim so I'm building from the ground up.

So far I've been able to make an ugly switchboard on a screen, allowing a user to connect the operator to the caller (but not yet caller to callee).

I'm finding Github's project functionality helpful to plan out the development.