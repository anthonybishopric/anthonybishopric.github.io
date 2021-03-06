---
layout: post
title: Programming In The Dark
---
I climbed a very steep learning curve in my first startup that negatively affected the way I coded for years.

During my Chinese Literature class in the Spring semester of 2007, my phone rang - I let it go to voicemail. [Jeremy Welch](http://www.jeremyrwelch.com/) and I would talk later that night about starting a company called [Shoeboxed](http://shoeboxed.com). We had absurd, nonsensical goals for the product - a social network to share information about your purchases. I had not entertained the idea of being in a startup; at the time, I was a TA in a computer organization class and thought being in a startup might be a differentiator for me. After talking with my mom about the prospect of starting a company, I decided to go for it.

Fast-forward through 3 redbull powered all-nighters to hit our launch date, drama among founders, convincing skeptical friends, etcetera ad nauseum - but I really don't want to talk about it like that. I don't have any rose-tinted glasses for that time or for that experience. To some extent, this post is a cautionary tale about knowledge and how it can be gleaned over time. It is fundamentally about what it meant for me to be a programmer with no experience trying to build a sophisticated web product.

I first learned about programming languages^ in my freshman year of college. I had a natural love for it but my knowledge was necessarily limited by my experience. With only 2 years of intro-CS exposure, I entered the startup fray with very little ammunition for success. The scope of the project seemed overwhelming, the way asking a 5 year old to pay the family taxes would be overwhelming. There were so many intermediate steps I hadn't taken and I didn't have time to go through them.

The other cofounder Taylor emailed one of his more experienced friends for recommendations on a Java technology stack that might scale well - the response for which was Spring MVC and Hibernate. Unquestioningly, since I didn't know how to really question technology recommendations yet, I began to use these tools to build the web facing part of our site. Simultaneously, as though getting started on a J2EE stack wasn't going to be hard enough, someone else managed to convince me that regular expressions, which were going to be crucial to the application, needed to be optimized! So we added a whole bunch of Perl scripts to deal with the regular expression requirements of our project and used direct socket connections to pass along regex results. For hosting, we hooked up a laptop with a broken monitor to the Duke's network and memorized the IP address for when we needed to SSH into it. Later, we would rent a shitty VPS in Florida that yours truly would configure (I literally knew nothing about basic Unix commands). When that machine began to have kernel panics, I had never seen such things nor knew how to diagnose them. To share code amongst the engineers, we quietly used one of Duke Computer Science's machines and hosted CVS on it. And to top off the insanity, we maintained our own custom [Postfix](http://www.postfix.org/) implementation with custom Perl modules.

(In case you're curious what we were using all that awful technology for, check out this [hilarious review about our insane product](http://news.cnet.com/8301-13507_3-9812969-18.html). Shoeboxed has since, thankfully, pivoted into something sensible. There is something adorable about this kind of proto-social network startup hype nonsense baked into the first version of Shoeboxed that I find funny if nothing else.)

In some ways I had already achieved cargo cult programming eliteness in signing off on that architecture. For as naive as I was about building a company's engineering resources, [I knew that PHP was total shit](http://me.veekun.com/blog/2012/04/09/php-a-fractal-of-bad-design/) and we weren't even going to entertain the idea of building our awesome world-dominating startup on it. So I didn't pick the shitty, fast language and I over-structured the technology, based on loose and fast recommendations and very little thought. And so I entered the cave.

What followed were 4-5 months of excruciatingly painful "software" development. Shoeboxed had, at times, managed to recruit unpaid students to volunteer to do pieces of tech work, but I was the only engineer to see Shoeboxed through its first product, full-time. Tomas, another engineer^^, came close but had also taken an internship at Microsoft that summer, so he was noticeably absent for a few months. The only uninterrupted engineer in this process was myself, and I took the brunt of development on my shoulders.

I can't describe how awful it is to have to learn how to program alone in a Java stack. When I say alone, I also mean without a community or a team to go to. And unlike PHP, ^nothing^ is intuitive about developing a web application in Java, let along SpringMVC. These were the days when the framework supported _exactly one_ form on each page.

But to be clear, there were at least two reasons why I feel I was uniquely fucked by my situation.

Shoeboxed spent its first summer of life in Berlin, Germany. I'll save the rationale for that choice for a different post. A side effect of our location was the limited availability of broadband internet. And when I say limited, I mean it was nonexistent. For whatever bizarre labor laws, getting broadband internet installed in Berlin takes a month of lead time, so the first month of the summer spent in Berlin was without internet. We also moved apartments midway through and lost internet for yet another month. Altogether, we had dedicated internet in our office (which was also home) for 3 weeks. On Maslow's hierarchy of needs for a startup, having internet access is like breathing - you can't really operate at a higher order of thinking without it.

We got around this little problem by invading the [Sony center at Potsdamer Platz](http://en.wikipedia.org/wiki/Potsdamer_Platz), which had one of the only free, open wireless networks in the city. We took the train from Kreuzberg daily to get there, and we'd sit out on park benches, slamming the overburdened router. Disconnects were frequent, stress was high. But we got through it. Other days, when we were feeling particularly hedonistic, we'd wander over to a real honest-to-goodness internet cafe and paid what felt like incredible amounts of money to work online. In our first apartment, an ex-Soviet Bloc apartment complex, one of the tallest in the city, we found wireless in the stairwell a few floors down and we'd all crowd around in the well hijacking some poor person's wireless for hours. One time, I was alone down there and a janitor found me sitting there on my computer. Not knowing any German (or Russian), it was an awkward exchange to say the least.

I said there were two reasons why I was screwed. Besides a total internet blackout, the other major problem was a bizarre combination of hero mentality crashing into full on insecurity. The way I imagine most people going into, say, programming work as a freelancer, you already have some degree of _confidence_, if not expertise. With Shoeboxed, I did not - I was desperately insecure in the face of these horrifying technologies.

Have you ever stared at technical documentation for hours and had no idea what it said? I have. I don't know if it was some basic reading comprehension skills I lacked or expertise from years of learning how to read it, but most of the documentation I read went like this:

	SpringMVC is a tool that helps you structure your code well. Isn't that great?

	Good software is good, bad software is bad!

	IMPORTANT: The reification of praxis may be parsed as the systemization of the 
	image. Spring's aggressive appraisal of the relationship between the systemization
	of indeterminacy and the fragmentation of Struts' counter-functional ideology 
	reorients the field toward a more theory-driven perspective.

And with those last two sentences comes panting and swaying and a lack of confidence. Something very, very bad happened to me. A combination of insecurities, time pressure ("is the site done yet?") and working 16 hour days turned me into an intellectual recluse. Why was everything so complicated? Why can't I read this documentation? These words make no sense to me.

Of course [Spring's Documentation](http://static.springsource.org/spring/docs/2.0.x/reference/mvc.html) wasn't made of fake academic sentences. It was, however, written with an ex-Struts user in mind, which I most certainly was not. Hibernate wasn't much better, and this is a real example from a Hibernate 2 doc page:

	Let's start by adding a simple hello world example for our Book table.

	<?xml version='1.0' encoding='UTF-8'?>
	<!DOCTYPE hibernate-configuration PUBLIC
	        "-//Hibernate/Hibernate Configuration DTD 3.0//EN"
	        "http://hibernate.sourceforge.net/hibernate-configuration-3.0.dtd">
	<hibernate-configuration>
	    <session-factory>
	        <!-- Example mapping file inclusion -->
	        <mapping resource="org.example.Book.hbm.xml"/>

	    </session-factory>
	</hibernate-configuration>

	Next let's specify columns on the Book table...

The documentation was supposed to be my flashlight, but it didn't work^^^. So instead, I worked in the dark. I felt along walls and ran into things, knocked my head a few times and kept groping until I had a somewhat functioning website. That's exactly how you create terrible software - by not understanding what you're doing. I began to favor experimentation over documentation, partly because the documentation was impenetrable but also because I didn't trust myself to feel good about myself by the time I had finished reading it.

My _fear of manuals_ became habitual, compounded by a lack of internet connectivity that summer. I grew scar tissue around the idea that I could power through my technical challenges without thinking. It's taken years to undo that part of my developer personality. It wasn't until I started using Ruby on Rails that I realized how deeply biased I am towards experiential learning. Nowadays I am relieved to meet people who RTFM, because I perceive them to have greater patience and self-confidence than me. Nobody should have a mandate to experience every problem under the sun to learn, as very Lean as that may be. I shouldn't have to experience crippling data corruption because I didn't understand the difference between MyISAM and InnoDB. I shouldn't have to experience terrible database throttling in order to understand why you should never use a TreeSet for an unordered association in Hibernate. That's self-inflicted pain.

It's a habit that crosses into other crippling problems, like reinventing the wheel. If anyone tells you they've written a homegrown ORM/MVC framework/templating engine/lightweight version of JQuery, you should run away as fast as possible. But certainly worse than that is the isolation it imposes. Forgetting that people exist - that there are folks who could help you if you only engaged them - is a secondary symptom of this problem.

I'm not embarassed to admit that I have had this problem. It's impatience mixed with insecurity - I think a lot of developers have it. A strange side effect of so many people having it is the tech popscene effect, wherein everyone inexplicably crowds around a common technology because it's hip, not because it actually solves the problems they have. I see this with NoSQL stores and Node and Scala and Go and other things all the time.

In any case, that's how I was shaped as a self-taught developer. While I have been very grateful for my successes in startups, I don't like how this aspect of my developer personality formed. I now understand what people meant when they said I should start working at a bigger company to "see what it was like" before going off to do a startup - it's not process stuff, but communication and knowledge sharing skills that you can only learn when you work with others who have done it before. It reinforces why mentorship and open communication are so important in a team.

^ Not including [TI-BASIC](http://en.wikipedia.org/wiki/TI-BASIC) from high school days.

^^ Tomas is a good friend and current coworker at [Box](https://box.com)

^^^ At one point, we were having a problem where Hibernate's object proxying facility caused the Java runtime to crash outright. Not only was such a possibility horrifying as I had never left the protective shell of the JVM, but the advice we found on the forums was equally awful - one person told us we should have made our code abstract enough to allow us to refactor out Hibernate if necessary.