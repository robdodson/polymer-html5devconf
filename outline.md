Agenda
===

Where are we with the web today, how did we get here, what's around the corner (web components)

As we do that I'm going to talk about Web Components, what they are, how they actually work, and what Polymer's relationship is to them

Using Web Components to improve our process

Where are we
===

Moving into the multi-device world.

90% of users who begin a task on one device, later finish it on another one.

So that means that as designers and developers, we have to start looking at the things we build with an eye toward mobile. They aren't static anymore, they're reacting all the time.

As Andy Clarke put it: As an industry, we sell websites like paintings [blockquote slide]

Dave Rupert from Paravel has this wonderful blog post that you all should go read called Responsive Deliverables. And in it, he retells the story of how Paul Rand built up the Westinghouse brand, starting with a logo and color scheme and branched out into business cards, packaging, vehicles, etc. And there’s this one line that really stuck in my head, he said, referring to all of the branching out, that it was the sum of these components which made up the physical brand [blockquote slide]

And that's how we have to think about the things we build. We have to start thinking in design systems. How is this thing I’m building going to work on phone? or a tablet? or a...phablet? [sequence of device screenshots]

How’s it going to work when it’s 6 centimeters from someone’s eye, [screenshot glass]
or 16 feet away on their crazy 4K TV. [screenshot chromecast]

Dave goes on to say that we should be building mini-bootstraps, custom tailored to our client's needs.

So moving from rough ideas, to clickable prototypes and the things that eventually become our final applications and all along the way we're systemizing the design. We're breaking it into components, we're making sure they're responsive, performant, accessiblity. This is where I think Web Components can come in and help us evolve our processes so we're better prepared to deal with designing and developing for an infinite spectrum of screen sizes and the 5 *billion* mobile users we're expecting to activate in the coming years.

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

Comp => $(document).ready() => maverick

Style tiles? Element collage?
Living style guide
  - PatternLab
  - http://sfdc-styleguide.herokuapp.com/?id=isv#
  Anna Debenham, 24ways
    - easier to test
    - better workflow
    - shared vocabulary
    - useful reference
    - http://gim.ie/fZyK
  Hard to maintain
    - big orgs can dedicate people, what about small shops?
  Do one thing and do it well - molecules
Mocks
  - begin life as wireframes, increase fidelity over time
  - client facing / stakeholder facing
  - x-picture
Build prototypes
  - brings the team together
  - test the effectiveness of what you're building
  - design and iterate
  - test variations
  - in code
  "Pattern Lab is a collection of tools to help create and maintain atomic web design systems"
  "NOT a UI framework"
  Cloud Four, Common Patterns in Styleguides, Boilerplates and Pattern Libraries
  - pattern lab -> designer
Potentially share stuff
  - element collages
  - crazy idea!
