---
layout: post
title: TraceTrace - The Game
---

[A game entirely about clicking the dot](/tracetrace)

The game was my first exploration of [ProcessingJS](http://processingjs.org/). Processing, which is itself a Java-like language that wraps OpenGL, has been around for a long time; John Resig reimplemented Processing such that it can be interpreted by a Browser, making WebGL quite easy. When I get time I'll head back over to [Super Maze Wars](/supermazewars), which seems like it'd be very easy in Processing.

Being a somewhat brain damaged Java programmer, I enjoyed being able to use class inheritance out of the box. That said, for future work I think I'll try [PaperJS](http://paperjs.org/) instead, at least for 2d animations. Debugging in ProcessingJS is still a bit rough - I ran into a parse error in my Processing script that was not caught during interpretation, and instead crashed ProcessingJS altogether. As a result, I had to spend at least an hour digging through the ProcessingJS source to figure out what symbols it had crashed into when it encountered my error. That issue, along with generally unreliable stack traces made for slow going sometimes.