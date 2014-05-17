Intro
===

Dave Rupert from Paravel has this wonderful blog post that you all should go read called Responsive Deliverables. And in it, he retells the story of how Paul Rand built up the Westinghouse brand, starting with a logo and color scheme and branched out into business cards, packaging, vehicles, etc. And there’s this one line that really stuck in my head, he said, referring to all of the branching out, that it was the sum of these components which made up the physical brand [blockquote slide]

The main point of Dave’s post is to get people to start thinking of their designs in terms of components, and not just, as one commentator put it, “snapshots”. [screenshot of psd]

Because web design is no longer about creating a few static pages or handing off some comps. As Andy Clarke put it: As an industry, we sell websites like paintings [blockquote slide]

We’ve been selling ideas that fit neatly into one or two picture frames. But that doesn’t work in a multi-device world. We have to start thinking in design systems. How is this thing I’m building going to work on phone? or a tablet? or a...phablet? [sequence of device screenshots]

How’s it going to work when it’s 6 centimeters from someone’s eye, [screenshot glass]
or 16 feet away on their crazy 4K TV. [screenshot chromecast]

And so I think that in a year or two from now, we're going to look back on this time—or maybe we won't because maybe we'll have laser vision by then or something—but in a year or two web development is going to feel like a very different thing.

How we design our sites, the tools and processes that we use, are going to be very different. And how we develop our sites, that's going to be different as well...

And that's what I wanted to talk about today, how can we start preparing for the future now. What strategies can we use to improve our workflow and better collaborate, both designer and developer, to support the new multi-device landscape.

Because really, that's what this is all about. The trend toward mobile has set in motion all of these changes that we're now grappling with as an industry.

[mobile usage stat!]

This is a really important statistic that I want to impress upon you all because the multi-device world is here, it is happening, and even if you think your current site or application only makes sense on desktop, the longer you avoid updating your process to work in the multi-device world, the more you're doing your future self a disservice.

And a big part of that process is how we move from rough ideas, to clickable prototypes and the things that eventually become our final applications. This is where I think Web Components can come in and help us evolve our processes so we're better prepared to deal with designing and developing for an infinite spectrum of screen sizes and the 5 *billion* mobile users we're expecting to activate in the coming years.

But before I talk anymore about the future, I want to revisit the past a little bit so we can think about how we arrived where we currently are, and how we can move forward.

So, how many of you have seen this website before? ...

Now the content of the site itself is pretty silly but it proves a really interesting point. If we strip out CSS and JavaScript and we go waaaay back to the earliest days of the internet, we actually solve most of the problems we're dealing with today.

The page loads fast
It fits in any screen size (we solved responsive design before we had smart phones! so we somehow solved responsive design and then unsolved it)
Looks the same in all browsers
And it has accessibility built in

Most importantly, anyone in this room could build this site. Think about that for a moment.

And let's ask ourselves: why.
why is this so easy to build.

You've got <h2>... ok that makes a big header
<p> tag, yep that's a paragraph
<select>... select is really interesting. Anyone looking at this markup and what it renders can reverse engineer it in their head. Even if they've never written a line of code in their lives, this is easy to reason about. And select has some really interesting features to it.

It has styling, but... we didn't have to write CSS
It has encapsulation, we don't see the markup that makes it render its dropdown, and we can't write CSS to poke it in the eye and break its behavior or style.
It has a11y built in.
It has a programmatic API. There are properties like selectedIndex...
And it's composable. If we drop it inside a form element, suddenly we've created something much bigger and much more complex out of basic building blocks.

So what happened...



Living style guide
  - http://sfdc-styleguide.herokuapp.com/?id=isv#
  - PatternLab
Build prototypes
  - in code
  - designer
Potentially share stuff
  - crazy idea!
