title: about:me
id: who

<p class="avatar rounded"></p>

<p>Rob Dodson</p>
<p>Developer Advocate, <img src="images/logos/google_logo.png" style="height: 30px;margin: 0;"> <img src="images/logos/chrome_logo.png" style="height:27px;margin:0;vertical-align: top;"></p>

<p class="topmargin"></p>

<i class="icon icon-google-plus"></i>
<a rel="author" href="http://google.com/+RobDodson">google.com/+RobDodson</a>

<i class="icon icon-twitter"></i>
<a rel="author" href="http://twitter.com/rob_dodson">@rob_dodson</a>

<i class="icon icon-bookmark"></i> 
<a rel="author" href="http://robdodson.me">robdodson.me</a>

<aside class="note">
  <section>
    <p>Introduce yourself, mention contact info</p>
    <p>
      Quick show of hands, who here has heard of Polymer or Web Components?
    </p>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vleft

<h2 style="margin-top: 33%">Agenda</h2>

<aside class="note">
  <section>
    <ul>
      <li>Where are we with the web today, how did we get here, what's around the corner</li>
      <li>As we do that I'm going to talk about Web Components, what they are, how they actually work, and what Polymer's relationship is to them</li>
      <li>Using Web Components to improve our process</li>
    </ul>
  </section>
</aside>

---

body_class: platform-fill
content_class: flexbox vleft

<h2 style="margin-top: 33%">[shot of devices]</h2>

<aside class="note">
  <section>
    <p>This is what it's all about.</p>
    <p>Moving into the multi-device world.</p>
  </section>
</aside>

---

content_class: flexbox vcenter

<h2 style="font-size: 60px; line-height: 1.25;"><strong>90%</strong> of tasks begun on <strong>one device</strong> will end on <strong>a different one</strong>.</h2>

<aside class="note">
  <section>
    <p>Especially true for tasks that start on mobile devices like looking for a plane ticket or shopping.</p>
    <p>So that means that as designers and developers, we have to be engineering our sites so they have a continous experience from one screen device to the next.</p>
    <p>And we need a process to reason about our designs so they're flexible and evolving and work in this multi-device world.</p>
  </section>
</aside>

---

body_class: paravel

<aside class="note">
  <section>
    Dave Rupert from Paravel has this wonderful blog post that you all should go read called Responsive Deliverables. And in it, he retells the story of how Paul Rand built up the Westinghouse brand
  </section>
</aside>

---

body_class: westinghouselogo

<aside class="note">
  <section>
    Really simple geometric shapes. From that he built up a logo and color scheme and branched out into business cards
  </section>
</aside>

---

body_class: westinghousebulb

<aside class="note">
  <section>
    Packaging, vehicles, etc
  </section>
</aside>

---

body_class: camera
body_overlay: white
class: nobackground nopadding
content_class: flexbox vleft

<figure class="backdrop">
  <blockquote>
    &ldquo;The <strong>sum of these components</strong> made up the physical brand&rdquo;
  </blockquote>
  <figcaption>
    <cite><a href="http://daverupert.com/2013/04/responsive-deliverables/">Responsive Deliverables</a></cite>, Dave Rupert
  </figcaption>
</figure>

<aside class="note">
  <section>
    And that's how we have to think about the things we build. We have to start thinking of them as systems of components that live and react to different screen sizes and not just as static comps.
  </section>
</aside>

---

content_class: flexbox vcenter

<h2 style="font-size: 60px; line-height: 1.25;"><strong>Components</strong> &gt; Static Comps</h2>

<aside class="note">
  <section>
    How is this thing I’m building going to work on phone?
  </section>
</aside>

---

content_class: flexbox vcenter

<h2 style="font-size: 60px; line-height: 1.25;">[shot of phone and tablet]</h2>

---

content_class: flexbox vcenter

<h2 style="font-size: 60px; line-height: 1.25;">[shot of phablet]</h2>

---

content_class: flexbox vcenter

<h2 style="font-size: 60px; line-height: 1.25;">[shot of glass]</h2>

<aside class="note">
  <section>
    How’s it going to work when it’s 6 centimeters from someone’s eye
  </section>
</aside>

---

content_class: flexbox vcenter

<h2 style="font-size: 60px; line-height: 1.25;">[shot of chromecast]</h2>

<aside class="note">
  <section>
    Or 16 feet away on their crazy 4K TV
  </section>
</aside>

---

content_class: flexbox vcenter

<h2 style="font-size: 60px; line-height: 1.25;">Mini-bootstraps</h2>

<aside class="note">
  <section>
    Dave goes on to say that we should be building mini-bootstraps, custom tailored to our client's needs.
  </section>
</aside>

---

content_class: flexbox vcenter

<h2 style="font-size: 60px; line-height: 1.25;">idea => prototype => $$$</h2>

<aside class="note">
  <section>
    <p>So moving from rough ideas, to clickable prototypes and the things that eventually become our final applications and all along the way we're systemizing the design. We're breaking it into components, we're making sure they're responsive, performant, accessiblity</p>

    <p>This is where I think Web Components can come in and help us evolve our processes so we're better prepared to deal with designing and developing for an infinite spectrum of screen sizes and the 5 *billion* mobile users we're expecting to activate in the coming years.</p>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vleft

<h2 style="margin-top: 33%">Let's go back in time...</h2>

<aside class="note">
  <section>
    But before I talk anymore about the future, I want to revisit the past a little bit so we can think about how we arrived where we currently are, perhaps learn some lessons along the way.
  </section>
</aside>

---

id: netscape
#title: Understand where we came from
class: nobackdrop nobackground
#image: images/bgs/netscape_blank.png
content_class: flexbox vcenter
body_class: netscape


<template id="formexample" style="display: none">
  <style>body{margin:0;padding:0;}</style>
  <form>
    <table class="build" border="10" cellpadding="5" cellspacing="5">
    <tr><td><label>First name:</td><td><input type="name"></td></tr>
    <tr><td><label>Last name</td><td><input type="name"></label></td></tr>
    <tr><td>T-shirt size</td><td>
      <select>
        <option>Small</option>
        <option selected>Medium</option>
        <option>Large</option>
        <option>X-large</option>
      </select>
    </td></tr>
    <tr><td><label>Gender</label></td><td>Male: <input type="radio"  name="gender"> Female: <input type="radio" name="gender"></td></tr>
    <tr><td colspan="2"><input type="submit"></td></tr>
    </table>
  </form>
</template>

<iframe id="formframe" style="width:300px;border:none;height:240px;"></iframe>

<script>
  var clone = document.querySelector('#formexample').content.cloneNode(true);
  var div = document.createElement('div');
  div.appendChild(clone);
 document.querySelector('#formframe').srcdoc = div.innerHTML;
</script>

<aside class="note">
  <section>
    <p>So this is everyone's first website. And you might be looking at it like "uh yeah ok whatever" but it demonstrates a few interesting point</p>
    <p>If we strip out CSS and JavaScript and we go waaaay back to the earliest days of the internet, we actually solve most of the problems we're dealing with today.</p>
    <ul>
      <li>The page loads fast</li>
      <li>It fits in any screen size (we solved responsive design before we had smart phones! so we somehow solved responsive design and then unsolved it)</li>
      <li>Looks the same in all browsers</li>
      <li>And it has accessibility built in</li>
    </ul>
    <p><strong>Most importantly, anyone in this room could build this site. Think about that for a moment.</strong></p>
    <p>And let's ask ourselves: why. why is this so easy to build?

    You've got h2... ok that makes a big header
    p tags... yup that's a paragraph
    And then you've got select
  </section>
</aside>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight">
&lt;select>
  &lt;option>Small&lt;/option>
  &lt;option>Medium&lt;/option>
  &lt;option>Large&lt;/option>
&lt;/select>
</pre>

<select class="corner top right">
  <option>Small</option>
  <option>Medium</option>
  <option>Large</option>
</select>

<aside class="note">
  <section>
    <p>select is really interesting. Anyone looking at this markup and what it renders can reverse engineer it in their head. Even if they've never written a line of code in their lives, this is easy to reason about. And select has some really interesting features to it.</p>
    <ul>
      <li>It has styling, but... we didn't have to write CSS</li>
      <li>It has encapsulation, we don't see the markup that makes it render its dropdown, and we can't write CSS to poke it in the eye and break its behavior or style.</li>
      <li>It has a11y built in.</li>
      <li>It has a programmatic API. There are properties like selectedIndex...</li>
      <li>And it's composable. If we drop it inside a form element, suddenly we've created something much bigger and much more complex out of basic building blocks.</li>
    </ul>
  </section>
</aside>

---

content_class: flexbox vcenter

<h2>Elements are the building blocks of the web</h2>
<img src="./images/screenshots/legos.png" style="position: absolute; bottom: -500px; right: -350px;">

---

hidden: true
body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded">Elements are <em>configurable</em></h2>

---

hidden: true
class: large
content_class: flexbox vcenter

<pre class="nohighlight">
&lt;select id="schwag">
  ...
  &lt;option <b>disabled</b>>Medium&lt;/option>
  &lt;option <b>disabled</b>>Large&lt;/option>
  &lt;option <b>selected</b>>XX-large&lt;/option>
&lt;/select>
</pre>

<select id="schwag" class="corner top right">
  <option disabled>Small</option>
  <option disabled>Medium</option>
  <option disabled>Large</option>
  <option selected>XX-large</option>
</select>

---

hidden: true
class: large
content_class: flexbox vcenter

<pre class="nohighlight" style="margin-left: -100px;">
&lt;select <b>size="4"</b> <b>multiple</b>>
  &lt;option>Do&lt;/option>
  &lt;option>Re&lt;/option>
  &lt;option>Mi&lt;/option>
  ...
&lt;/select>
</pre>

<select size="4" multiple class="corner top right">
  <option>Do</option>
  <option>Re</option>
  <option>Mi</option>
  <option>Fa</option>
  <option>So</option>
  <option>La</option>
  <option>Ti</option>
  <option>Do</option>
</select>

---

hidden: true
class: large
content_class: flexbox vcenter


<pre class="nohighlight">
&lt;select>
  &lt;option>Small&lt;/option>
  <s>&lt;li>Medium&lt;/li></s>
  &lt;option>Large&lt;/option>
&lt;/select>
</pre>

<select class="corner top right">
  <option>Small</option>
  <li>Medium</li>
  <option>Large</option>
</select>

---

hidden: true
body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded">Elements are <em>composable</em></h2>

---

hidden: true
class: large
content_class: flexbox vcenter

<pre class="nohighlight">
&lt;select>
  &lt;optgroup label="German Cars">
    &lt;option>Mercedes&lt;/option>
    &lt;option>Audi&lt;/option>
  &lt;/optgroup>
  ...
&lt;/select>
</pre>

<select class="corner top right">
  <optgroup label="German Cars">
    <option value="mercedes">Mercedes</option>
    <option value="audi">Audi</option>
  </optgroup>
  <optgroup label="American cars">
    <option value="ford">Ford</option>
    <option value="gm">GM</option>
  </optgroup>
</select>

---

hidden: true
class: large
content_class: flexbox vcenter

<pre class="nohighlight">
<b>&lt;form></b>
  &lt;select name="size">
    &lt;option value="s">Small&lt;/option>
    &lt;option value="m">Medium&lt;/option>
    &lt;option value="l">Large&lt;/option>
  &lt;/select>
<b>&lt;/form></b>
</pre>

---

hidden: true
body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded">Elements are <em>programmable</em></h2>

---

hidden: true
class: large
content_class: flexbox vcenter

<pre class="nohighlight">
var foo = mySelect.selectedIndex;
</pre>

---

body_class: core-fill
content_class: flexbox vleft

<h2 style="margin-top: 33%">So what happened?</h2>

---

title: This happened
body_class: readable
class: nobackground highlight

<aside class="note">
  <section>
    <p>This happened.</p>
    <p>The language wasn't expressive</p>
    <p>We've had to work around what the browser does not give us</p>
  </section>
</aside>

---

id: tab-examples
title: Building UI today

<div class="build flexbox vcenter centered">
<img src="images/screenshots/tabs/jquery.png">
<img src="images/screenshots/tabs/kendo.png">
<img src="images/screenshots/tabs/yui.png">
<img src="images/screenshots/tabs/angular.png">
<img src="images/screenshots/tabs/sencha.png">
<img src=""> <!-- intentional. holder to see all images together -->
</div>

<aside class="note">
  <section>
    <p>Now that we're seeing this JavaScript renaissance...</p>
    <p>I think it's unfortunate for two reasons:</p>
    <p>1) <strong>You're putting yourself into a silo</strong></p>
    <p>2) <strong>You make it harder for designers and new developers to join in</strong></p>
  </section>
</aside>

---

body_class: paralysis

<aside class="note" style="z-index: 1000">
  <section>
    <p>It's gotten to the point where Addy is writing article's like this</p>
    <p>We're so scared of making the wrong choice and picking the wrong UI framework
    <p>It's causing us to grind to a halt as we struggle to solve the same problems over and over.</p>
  </section>
</aside>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight" style="margin-top: -50px;">
&lt;x-tabs&gt;
  &lt;x-tab&gt;Tab 1&lt;/x-tab&gt;
  &lt;x-tab&gt;Tab 2&lt;/x-tab&gt;
  &lt;x-tab&gt;Tab 3&lt;/x-tab&gt;
&lt;/x-tabs&gt;
</pre>

<aside class="note">
  <section>
    <p><b>Not possible, until Web Components!</b></p>
  </section>
</aside>

---

content_class: flexbox vleft

<h2 style="font-size: 60px; line-height: 1.25;">Web Components are a set of <strong>emerging standards</strong> that allow developers to <strong>extend HTML</strong>.</h2>

<aside class="note">
  <section>
    <p>Let me show you an example of how this works in practice...</p>
  </section>
</aside>

---

hidden: true
title: Creating a carousel
subtitle: The old way

<pre class="prettyprint" style="font-size:21px; line-height: 1.2; height: 500px; overflow-y: scroll;" data-lang="HTML">
&lt;div id="carousel"&gt;
  &lt;input checked="" type="radio" name="carousel" id="slide1"&gt;
  &lt;input type="radio" name="carousel" id="slide2"&gt;
  &lt;input type="radio" name="carousel" id="slide3"&gt;
  &lt;div id="slides"&gt;
    &lt;div id="overflow"&gt;
      &lt;div class="inner"&gt;
        &lt;article&gt;
          &lt;img src="sunset.jpg" alt="a dramatic sunset"&gt;
        &lt;/article&gt;
        &lt;article&gt;
          &lt;img src="arch.jpg" alt="a rock arch"&gt;
        &lt;/article&gt;
        &lt;article&gt;
          &lt;img src="hills.jpg" alt="some neat hills"&gt;
        &lt;/article&gt;
      &lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
  &lt;label for="slide1"&gt;&lt;/label&gt;
  &lt;label for="slide2"&gt;&lt;/label&gt;
  &lt;label for="slide3"&gt;&lt;/label&gt;
&lt;/div&gt;
</pre>

<aside class="note">
  <section>
    <p>This is how we create our UI today. There's a ton of boilerplate and most of these elements are just structural markup</p>
  </section>
</aside>

---

hidden: true
title: Creating a carousel
subtitle: The Web Components way

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;img-carousel&gt;
  &lt;img src="sunset.jpg" alt="a dramatic sunset"&gt;
  &lt;img src="arch.jpg" alt="a rock arch"&gt;
  &lt;img src="hills.jpg" alt="some neat hills"&gt;
&lt;/img-carousel&gt;
</pre>

<aside class="note">
  <section>
    <p>With Web Components we can do something like this. Usign the img-carousel tag, I can just add the information that's relevant to *my* application, and forget about all the boilerplate.</p>
  </section>
</aside>

---

title: Video's secret DOM
subtitle: Be like the browser makers
content_class: flexbox vcenter

<video style="width: 55%; margin-top: -15%" src="foo.webm" controls>
</video>
<br>
<pre class="prettyprint" style="font-size:30px; line-height: 1.2;">
&lt;video src="foo.webm" controls&gt;&lt;/video&gt;
</pre>

---

body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Custom tags</em> + <em>Scoped styles</em> + <em>Encapsulation</em></h2>

<aside class="note">
  <section>
    <p>From a high level, these are the sexy selling points of Web Components</p>
  </section>
</aside>

---

hidden: true
content_class: flexbox vleft

<h2 style="font-size: 60px; line-height: 1.25;">That's cool. <strong>Why</strong> do I care?</h2>

---

class: nobackdrop nobackground browser-support
content_class: flexbox vcenter

<div class="flexbox">
  <h2>Templates</h2>
  <div class="browser-support-row">
    <div class="supported"><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>Custom Elements</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported partial"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>Shadow DOM</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported partial"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>HTML Imports</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported partial"><img src="images/logos/chrome_logo.png"></div>
    <div><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<aside class="note">
  <section>
    <p>There's no one Web Components technology, it's actually 4 different technologies which collectively form the Web Components umbrella</p>
    <ul>
      <li>Templates give you the ability to create reusable bits of DOM markup. If you've used a library like handlebars or mustache before then it should feel familiar. The difference now is that there is an actual &lt;template&gt; tag in the browser</li>
      <li>Custom elements give you the ability to create your own custom HTML elements. The x-tabs example from before is an instance of a custom element.</li>
      <li>Shadow DOM is the ability to create scoped styles and encapsulated markup. So you can put some HTML and CSS inside of the Shadow DOM and you're guaranteed your element will render as intended.</li>
      <li>Finally HTML Imports give you the ability to load external HTML files into your document. These files can contain resources like CSS, JavaScript and (most likely) custom element defintions.</li>
    </ul>
    <p>Talk about support chart. It's good, but developers won't use Web Components until they're supported in *all* browsers. But we want developer feedback before we ship these things. For that reason we created Polymer.</p>
  </section>
</aside>

---

class: nobackdrop nobackground yum
content_class: flexbox vcenter centered

<img src="images/logos/lockup.svg" style="height:180px;">

---

content_class: flexbox vleft

<h2 style="font-size: 60px; line-height: 1.25;">Polymer <strong>enables</strong> the use of Web Components</strong> in all <strong>modern browsers</strong>.</h2>

<!-- font-size: 42px; width: 52%; line-height: 1.3; -->

<aside class="note">
  <section>
    <p>It gives you the power of web components today</p>
    <p>You can start working with them and give feedback to the browser makers</p>
    <p>So... how do we do that?</p>
  </section>
</aside>

---

id: layers-of-polymer
class: polymer-diagram
title: Layers of Polymer

<div id="blocks-3d">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

<div class="build diagram-explanations">
  <div id="diagram-animate-in" data-build-index="1"></div>
  <div id="diagram-explode" data-build-index="2"></div>

  <div id="diagram-elements" class="diagram-explanation" data-build-index="6">
    <h3 class="elements bold">Elements</h3>
    <p>Reusable custom elements (in progress)</p>
  </div>

  <div id="diagram-polymer" class="diagram-explanation" data-build-index="5">
    <h3 class="core bold">Polymer</h3>
    <p>An opinionated way to work with Web Components</p>
  </div>

  <div id="diagram-platform" class="diagram-explanation" data-build-index="4">
    <h3 class="platform bold">Platform</h3>
    <p>Web Components polyfills for all <br>modern browsers</p>
  </div>

  <div id="diagram-native" class="diagram-explanation" data-build-index="3">
    <h3 class="bold">Native</h3>
    <p>The current browser landscape</p>
  </div>

  <div id="diagram-contract" data-build-index="7"></div>
  <div id="platform-shrink" data-build-index="8"></div>
</div>

<aside class="note">
  <section>
    <p>Here's a breakdown of how we add support for Web Components into all browsers</p>

    <ul>
      <li>Native: We start off with whatever level of support your current browser has. If that's something like mobile safari it might mean there's no support for web components at all!</li>
      <li>Platform: Polyfills web component support and jumps everyone into the future so they can start creating their own elements</li>
      <li>Polymer: Features and sugars. Things not on the standards track but we think are awesome so we include them. Two-way data binding, automatic node finding and a great declarative syntax</li>
      <li>Elements: Lastly, we include a set of pre-built elements which are ready to be dropped into any project</li>
    </ul>
  </section>
</aside>

---

hidden: true
id: evaporate-platform
class: polymer-diagram

<div id="blocks-3d">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

<div class="diagram-explanations" style="margin-top: 250px;">
  <div class="diagram-explanation">
    <h3 style="font-size: 35px; line-height: 1.5;">As browsers implement the specifications supported by the platform, the need for this <br>layer <strong>decreases</strong>.</h3>
  </div>
  <div class="build">
    <div id="platform-shrink" class="diagram-explanation">
      <h3 style="font-size: 35px; line-height: 1.5;">...till eventually it's all <strong>gone</strong>.</h3>
    </div>
  </div>
</div>

---

hidden: true
id: philosophy
title: Three ways to work with Polymer
build_lists: true
class: large
#content_class: flexbox vcenter

<div class="build topmargin">
  <div>
    <h3><b class="elements">Using</b> elements</h3>
    <br>
  </div>
  <div>
    <h3><b class="core">Creating</b> elements</h3>
    <br>
  </div>
  <div>
    <h3>Utilizing the modern web <b class="platform">platform</b></h3>
    <br>
  </div>
</div>

---

hidden: true
content_class: flexbox vcenter

<h2>Three ways to work with Polymer</h2>

---

body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Using</em> elements</h2>

---

hidden: true
body_class: platform-fill
content_class: flexbox vcenter

<h2 class="faded">Utilizing the modern web <em>platform</em></h2>

---

hidden: true
id: using-elements
title: Using <label class="elements">elements</label>
subtitle: <a href="http://www.polymer-project.org/docs/elements/" class="nounderline">polymer-project.org/docs/elements/</a>
class: nobackdrop nobackground segue elements polymer-diagram
keep_content: true

<div id="blocks-3d" class="in" style="top: 10%;">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

---

hidden: true
body_class: elements-fill
content_class: flexbox vcenter

<h2 style="font-size: 55px; letter-spacing: 0;">Everything is an element</h2>

<aside class="note">
  <section>
    <p><b>We want you to reach for the element</b></p>
  </section>
</aside>

---

id: polymer-ui-elements
title: UI elements

<div class="pull-right flexbox vcenter" style="width: 40%;margin-top:-100px;">
  <img src="images/polymer/uielements/polymer-ui-tabs.png" style="width:100%">
  <div class="flexbox vcenter" style="height:auto;">
  <img src="images/polymer/uielements/sidebarmenu.png">
  <img src="images/polymer/uielements/polymer-ui-toggle-button.png" style="margin-left:20px;">
  </div>
  <img src="images/polymer/uielements/toolbar.png" style="width:100%">
</div>

`<core-header-panel>` [demo](http://polymer.github.io/core-header-panel/components/core-header-panel/demo.html)

`<core-drawer-panel>` [demo](http://polymer.github.io/core-drawer-panel/)

`<core-overlay>`

`<core-tooltip>`

`<core-toolbar>`

`<core-menu>`

`<core-transition>` 

`<core-menu>`

`<core-list>`

`<core-iconset>`

`<core-action-icons>`

<aside class="note">
  <section>
    <p>Stress that elements are experimental (and visually disjointed) but let them know we're building something real.</p>
    <p>To help you out we've created some reusable UI elements. So we have things like polymer-ui-card (click on link and show demo), which is a nice swipeable Google Now style card</p>
    <p>We've also got polymer-ui-sidebar, (click on link and show demo) which is your classic expanding/collapsing sidebar</p>
    <p>And yes, we even include our own version of tabs!</p>
  </section>
</aside>

---

title: Everything is an element
subtitle: Core Toolbar

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install Polymer/polymer" data-tooltip="bower install Polymer/polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install Polymer/core-toolbar" data-tooltip="bower install Polymer/core-toolbar">core-toolbar.html</span>">
&lt;link rel="import" href="<span alt="bower install Polymer/core-icon-button" data-tooltip="bower install Polymer/core-icon-button">core-icon-button.html</span>">
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;core-toolbar&gt;
  &lt;core-icon-button icon="menu"&gt;&lt;/core-icon-button&gt;
  &lt;div core-flex&gt;My App&lt;/div&gt;
  &lt;core-icon-button icon="dots"&gt;&lt;/core-icon-button&gt;
&lt;/core-toolbar&gt;
</pre>

<div class="component-demo">
<link rel="import" href="bower_components/core-toolbar/core-toolbar.html">
<link rel="import" href="bower_components/core-icon-button/core-icon-button.html">
<output>
  <core-toolbar style="background: #7FDBFF">
    <core-icon-button icon="menu"></core-icon-button>
    <div core-flex>My App</div>
    <core-icon-button icon="dots"></core-icon-button>
  </core-toolbar>
</output>

</div>

<aside class="note">
  <section>
    <p>So this is the polymer-tabs element. To load it into your application you just import the polymer-ui-tabs.html file using an html import (point out we're doing that in the top right corner) and then the element is ready to use. No setup necessary!</p>
  </section>
</aside>

---

hidden: true
id: polymer-ui-collapsible-demo
title: Everything is an element
subtitle: Collapsible elements

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-ui-elements" data-tooltip="bower install polymer-ui-elements">polymer-ui-collapsible.html</span>">
</pre>

<pre class="prettyprint" style="font-size:25px;" data-lang="HTML">
&lt;polymer-ui-collapsible&gt;
  &lt;h3 class="polymer-ui-collapsible-header"&gt;Click Me!&lt;/h3&gt;
  &lt;div&gt;
    some content...
  &lt;/div&gt;
&lt;/polymer-ui-collapsible&gt;
</pre>

<div class="component-demo" style="height:100%">
<link rel="import" href="bower_components/polymer-ui-collapsible/polymer-ui-collapsible.html">
<output>
  <polymer-ui-collapsible>
    <h3 class="polymer-ui-collapsible-header" style="font-weight: bold;">Click Me!</h3>
    <p style="font-size: 18px; line-height: 1.4;">
      Realm of the galaxies at the edge of forever, made in the interiors of collapsing stars dispassionate extraterrestrial observer, rings of Uranus extraplanetary rich in heavy atoms shores of the cosmic ocean, white dwarf finite but unbounded!
    </p>
    <p style="font-size: 18px; line-height: 1.4;">
      Realm of the galaxies at the edge of forever, made in the interiors of collapsing stars dispassionate extraterrestrial observer, rings of Uranus extraplanetary rich in heavy atoms shores of the cosmic ocean, white dwarf finite but unbounded!
    </p>
  </polymer-ui-collapsible>
</output>

</div>

---

hidden: true
id: polymer-ui-toggle-button-demo
title: Everything is an element
subtitle: Toggle Button Element

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-ui-elements" data-tooltip="bower install polymer-ui-elements">polymer-ui-toggle-button.html</span>">
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-ui-toggle-button offcaption="Nope"&gt;
&lt;/polymer-ui-toggle-button&gt;
</pre>

<div class="component-demo">
<link rel="import"
  href="bower_components/polymer-ui-toggle-button/polymer-ui-toggle-button.html">

<output style="zoom: 2.5;">
  <polymer-ui-toggle-button offcaption="Nope"></polymer-ui-toggle-button>
</output>

</div>

---

hidden: true
body_class: elements-fill
content_class: flexbox vcenter

<h2>You don't have to know about their internals</h2>

---

title: Non-visual Elements
content_class: columns-2

<span class="bold blue">Layout</span>

`<core-layout>`

`<core-layout-grid>`

`<core-layout-trbl>`

<span class="bold blue">View</span>

`<core-media-query>`

`<core-pages>`

<span class="bold blue">Services / libs</span>

`<core-shared-lib>`

`<core-firebase>`

<span class="bold blue">Data</span>

`<core-localstorage>`

`<core-ajax>`

`<polymer-jsonp>`

`<polymer-file>`

`<polymer-meta>` 

<span class="bold blue">Behavior / interaction</span>

`<polymer-signals>`

`<core-selector>`

---

id: core-layout-demo
title: Everything is an element
subtitle: flexbox...using DOM

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install Polymer/polymer" data-tooltip="bower install Polymer/polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install core-layout" data-tooltip="bower install core-layout">core-layout.html</span>">
</pre>

<pre class="prettyprint" style="font-size: 30px; line-height: 1.2;" data-lang="HTML">
&lt;core-layout <b data-action="vertical">vertical</b>>
  &lt;div>Header&lt;/div>
  &lt;div <b data-action="core-flex">core-flex</b>>Body&lt;/div>
  &lt;div>Footer&lt;/div>
&lt;/core-layout>
</pre>


<div class="component-demo" style="height:100%">
<link rel="import" href="bower_components/core-layout/core-layout.html">
<output>
  <core-layout vertical title="Click me to add children">
    <div>Header</div>
    <div core-flex>Body</div>
    <div>Footer</div>
  </core-layout>
</output>

</div>

<aside class="note">
  <section>
    <p>Here's an example: This is polymer-flex-layout, which contains all the functionality of CSS flexbox in an easy to use tag. Toggle the vertical attribute to lay children out horizontally. Toggle the flex attribute to make your child fill as much space as it can.</p>
    <p>This demonstrates an important point about Web Components and what you can do when you're able to extend the platform. It gives you the power to create your own things if you're not satisfied with the current implementation in the browser. Flexbox is too complicated so why not make it easier.</p>
  </section>
</aside>

---

hidden: true
id: polymer-ajax-demo
title: Everything is an element
subtitle: AJAX...using DOM

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-ajax.html</span>">
</pre>

<pre class="prettyprint" style="font-size:25px;">
<b>&lt;polymer-ajax url="http://gdata.youtube.com/feeds/api/videos/"
              params='{"q":"chrome", "alt":"json"}'>
&lt;/polymer-ajax></b>
</pre>

<pre class="prettyprint" data-lang="JS" data-run-demo>
var ajax = document.querySelector('polymer-ajax');
ajax.addEventListener(<b>'polymer-response'</b>, function(e) {
  console.log(JSON.parse(<b>this.response</b>).feed.entry);
});
<b>ajax.go();</b>
</pre>

<div class="component-demo">
<link rel="import" href="bower_components/polymer-ajax/polymer-ajax.html">
<output><div>Hit run...</div></output>
</div>

<aside class="note">
  <section>
    <p>We have link tags and script tags which pull in external resources...</p>
    <p>Elements are composable</p>
  </section>
</aside>

---

hidden: true
content_class: flexbox vcenter

<h2>They're easy to add to your project</h2>

---

body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Creating</em> elements</h2>

<aside class="note">
  <section>
    <p>We've talked a bit about using elements, now let's look at how you can create your own elements. Polymer is going to make this really easy for you!</p>
  </section>
</aside>

---

hidden: true
id: creating-elements
title: Creating <label class="core">elements</label>
subtitle: <a href="http://www.polymer-project.org/polymer.html" class="nounderline">polymer-project.org/polymer.html</a>
class: nobackdrop nobackground segue core polymer-diagram
#content_class: flexbox vcenter
keep_content: true

<div id="blocks-3d" class="in" style="top: 10%;">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

<aside class="note">
  <section>
    <p><b>Polymer is going to make this really easy for you</b></p>
  </section>
</aside>

---

hidden: true
body_class: core-fill
content_class: flexbox vcenter

<h2 style="font-size: 55px; letter-spacing: 1.2;">Everything is an element</h3>

<aside class="note">
  <section>
    <p><b>Stop yourself and think, can I bundle this up into an element</b></p>
    <p><b>Polymer is going to make that really easy for you</b></p>
  </section>
</aside>

---

hidden: true
body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Declarative</em> element registration</h2>

<aside class="note">
  <section>
    <p>The declarative syntax that Polymer enables makes it super simple to start defining your own tags.</p>
  </section>
</aside>

---

id: declarative-registration
title: Declarative registration
#subtitle: Declarative registration

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.html</span>">
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-element name="my-element" <b>noscript</b>&gt;
  &lt;template&gt;
    &lt;style&gt;h2 { color: orange; }&lt;/style&gt;
    &lt;h2&gt;Hello from my-element!&lt;/h2&gt;
  &lt;/template&gt;
&lt;/polymer-element&gt;
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;my-element&gt;&lt;/my-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px;">
    <my-element></my-element>
  </output>
</div>

<aside class="note">
  <section>
    <p>This is a Polymer element definition. It's important to indicate that the name attribute must have a dash in it. That's to prevent future versions of HTML from stepping on your tag.</p>
    <p>Anything inside of the template will be stamped out when the parser sees your new tag</p>
    <p>Note that the style tag is *not* affecting the h2 at the top of the slide that says "Declarative Registration". That's because the styles are scoped by the Shadow DOM</p>
    <p>Mention noscript. That attribute tells Polymer that you're not including any JavaScript with your element.</p>
  </section>
</aside>

---

id: declarative-registration-proto
title: Declarative registration
#subtitle: Declarative registration with prototypes

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.html</span>">
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-element name="hello-element"&gt;
  &lt;template&gt;
    &lt;h2&gt;I can say hello&lt;/h2&gt;
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('hello-element', {
    sayHello: function() { alert('Howdy folks!'); }
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px;">
    <hello-element></hello-element>
  </output>
</div>

<aside class="note">
  <section>
    <p>If you do want to include JavaScript with your element you can omit the noscript attribute and include a script tag that calls the Polymer constructor.</p>
    <p>The Polymer constructor requires that you pass in your element's name, and a protoyper object. Properties and methods that you add to this prototype object are available on every instance of your new tag.</p>
    <p>In this example I've added some code to the page that listens for click events and calls target.sayHello().  (click on the elements)</p>
    <p>So easy to create an API for your element... but I want to add some data to this thing!</p>
  </section>
</aside>

---

hidden: true
body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Binding</em> expressions</h2>

<aside class="note">
  <section>
    <p>To work with data in an element we use binding expressions</p>
  </section>
</aside>

---

hidden: true
id: two-way-binding
title: Binding Expressions

<pre class="prettyprint" style="font-size:27px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-element name="owner-element"&gt;
  &lt;template&gt;
    &lt;h2&gt;<b>{{owner}}</b> built me with Polymer&lt;/h2&gt;
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('owner-element', {
    <b>owner: 'Rob'</b>
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;owner-element&gt;&lt;/owner-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px;">
    <owner-element></owner-element>
  </output>
</div>

<aside class="note">
  <section>
    <p>In this example we're using mustache syntax to bind the value owner in our template, to a property on our prototype.</p>
    <p>Press the 'h' key to focus the slide</p>
    <p>When this element renders, you'll see 'Rob built me with Polymer'.</p>
    <p>But elements are supposed to be configurable, so how do we let the user set the value of owner?</p>
  </section>
</aside>

---

hidden: true
body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Published</em> properties</h2>

<aside class="note">
  <section>
    <p>To do that we've created published properties</p>
  </section>
</aside>

---

hidden: true
id: published-properties
title: Published properties

<pre class="prettyprint" style="font-size:27px; line-height: 1.2;">
&lt;polymer-element name="owner-element" <b>attributes="owner"</b>&gt;
  &lt;template&gt;
    &lt;h2&gt;<b>{{owner}}</b> built me with Polymer&lt;/h2&gt;
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('owner-element', {
    <b>owner: 'Rob'</b>
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<pre class="prettyprint" style="font-size:27px; line-height: 1.2;">
&lt;owner-element <b>owner="Alex"</b>&gt;&lt;/owner-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px;">
    <owner-element owner="Alex"></owner-element>
  </output>
</div>

<aside class="note">
  <section>
  <p>Notice the attributes attribute I've created at the end of my polymer-element. That allows me to expose the owner property from my prototype to the outside world.</p>
  <p>This property is now 2-way data bound</p>
  <p>Now when someone uses our tag they can configure owner and set it to 'Alex', which renders: 'Alex built me with Polymer'</p>
  <p>So we've got a bit of data in here, how about interactivity?</p>
  </section>
</aside>

---

hidden: true
body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded">Declarative <em>event handlers</em></h2>

<aside class="note">
  <section>
    <p>To quickly add interactivity we can use declarative event handlers</p>
  </section>
</aside>

---

hidden: true
id: declarative-event-handlers
title: Declarative Event Handlers

<pre class="prettyprint" style="font-size:27px; line-height: 1.2;">
&lt;polymer-element name="click-element"&gt;
  &lt;template&gt;
    <b>&lt;button on-click="{{setMessage}}"&gt;Click me&lt;/button&gt;</b>
    <b>&lt;span&gt;{{message}}&lt;/span&gt;</b>
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('click-element', {
    <b>message: 'Waiting to be clicked...'</b>
    <b>setMessage: function() { this.message = 'I was clicked!' }</b>
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px; zoom: 2;">
    <click-element></click-element>
  </output>
</div>

<aside class="note">
  <section>
    <p>You can press h to focus the slide</p>
    <p>To add a bit of interactivity we can use a declarative event handler. Here we're using on-click (note, not onclick) to fire an action called setMessage any time our button is clicked.</p>
    <p>setMessage will change a property on our prototype called message, which will then update inside the binding in our template</p>
    <p>Explain why onclick is bad but on-click is awesome</p>
    <p>onclick is bad because it works in the global scope and uses eval. on-click is awesome because it only has access to your element, it automatically removes the event listener when your element leaves the DOM, and it uses polymer-gestures, a library which unifies mouse, touch and pointer events.</p>
  </section>
</aside>

---

hidden: true
body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded">Automatic <em>node finding</em></h2>

---

hidden: true
id: automatic-node-finding
title: Automatic Node Finding

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;">
&lt;polymer-element name="focus-element"&gt;
  &lt;template&gt;
    <b>&lt;button on-click="{{setFocus}}"&gt;Set Focus&lt;/button&gt;</b>
    <b>&lt;input id="nameInput" type="text"&gt;</b>
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('focus-element', {
    <b>setFocus: function() { this.$.nameInput.focus(); }</b>
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px; zoom: 2;">
    <focus-element></focus-element>
  </output>
</div>

<aside class="note">
  <section>
    <p>Explain why id's are bad but these are awesome</p>
  </section>
</aside>

---

hidden: true
title: Polymer features
subtitle: declarative web components

- Declarative element registration: `<polymer-element>`
- Declarative inheritance: `<polymer-element extends="...">`
- Declarative two-way data-binding: `<input id="input" value="{{foo}}">`
- Declarative event handlers: `<button on-click="{{handleClick}}">`
- Published properties: `xFoo.bar = 5 <-> <x-foo bar="5">`
- Property change watchers: `barChanged: function() {...}`
- Automatic node finding: `this.$.input.value = 5`
- PointerEvents / PointerGestures by default
- Support for Web Animations

<div class="build centered bold topmargin blue">
<span style="font-size:50px;">Be declarative. Write less code.</span>
</div>

<aside class="note">
  <section>
    <p>Registering your own element is kind of a wordy, verbose process</p>
    <p>You want to have a super button that inherits from your base button</p>
    <p>Two-way binding is awesome. You'll be amazed at how easy it is to build an entire application with nothing but binding</p>
    <p><b>We want to do things that make sense for developers</b></p>
  </section>
</aside>

---

hidden: true
id: more-complex-elements
title: Define an API
subtitle: complex elements require more juice...

<pre data-code-cycle class="prettyprint" data-lang="HTML" style="font-size:25px;line-height: 1.4;">
</pre>

<textarea selected>
<polymer-element name="my-input" noscript>
  <template>
    <input type="text" id="in" style="color: orange;">
  </template>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input">
  <template>
    <input type="text" id="in" style="color: orange;">
  </template>
  <script>Polymer('my-input');</script>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input">
  <template>
    <input type="text" id="in" style="color: orange;">
  </template>
  <script>
    Polymer('my-input', {
      get length() { return this.$.in.value.length; },
      ready: function() { ... }
    });
  </script>
</polymer-element>
</textarea>
<textarea>
&lt;polymer-element name="my-input">
  &lt;template>
    &lt;link rel="stylesheet" href="styles.css">
    &lt;input id="in" type="text">
  &lt;/template>
  &lt;script src="path/to/elements/myinput.js">&lt;/script>
&lt;/polymer-element>
</textarea>

- Properties/methods are added to `prototype`
- `this` refers to the element itself (e.g. `this.localName == "my-input"`)
- Can reference external scripts/stylesheets (e.g. CSP friendly)

<!-- <pre class="prettyprint" data-lang="HTML">
&lt;polymer-element name="my-input" constructor="MyInput">
  &lt;template>
    <b>&lt;link rel="stylesheet" href="styles.css"></b>
    &lt;input type="text">
  &lt;/template>
  <b>&lt;script src="path/to/elements/myinput.js">&lt;/script></b>
&lt;/polymer-element>
</pre> -->

---

hidden: true
id: published-properties
title: Publishing properties & data-binding
polymer_link: http://www.polymer-project.org/polymer.html#published-properties

2. **Inside** the element &rarr; use data-binding
2. **Outside** the element &rarr; users configure us using attributes

<pre data-code-cycle class="prettyprint" data-lang="HTML">
</pre>

<textarea selected>
<polymer-element name="my-input">
  <template>
    <input type="text" style="color: orange;">
  </template>
  <script>
    Polymer('my-input', {
      type: 'text', 
      color: 'orange'
    });
  </script>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input">
  <template>
    <input type="{{type}}" style="color: {{color}};">
  </template>
  <script>
    Polymer('my-input', {
      type: 'text', 
      color: 'orange'
    });
  </script>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input">
  <template>
    <input type="{{type}}" style="color: {{color}};" value="{{val}}">
    <polymer-localstorage name="myInputStorage" value="{{val}}"></polymer-localstorage>
  </template>
  <script>
    Polymer('my-input', {
      type: 'text', 
      color: 'orange'
    });
  </script>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input" attributes="type color">
  <template>
    <input type="{{type}}" style="color: {{color}};" value="{{val}}">
    <polymer-localstorage name="myInputStorage" value="{{val}}"></polymer-localstorage>
  </template>
  <script>
    Polymer('my-input', {
      type: 'text', 
      color: 'orange'
    });
  </script>
</polymer-element>
<my-input color="red"></my-input>
</textarea>

<!--
- User overrides `color` but `type` remains its default ("text")
- Since `val` isn't published, can't use it as a bindable attribute.
-->

---

hidden: true
title: Features in action
subtitle: responsive design...using DOM
#content_class: smaller 

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-media-query.html</span>">
</pre>

<pre class="prettyprint" data-lang="html">
&lt;polymer-element name="responsive-layout" attributes="responsive">
  &lt;template>
    <b>&lt;polymer-media-query query="max-width:640px" queryMatches="{{isPhone}}">&lt;/...</b>
    &lt;template if="{{isPhone && responsive}}"> &lt;!-- Phone markup -->
      &lt;content>&lt;/content>
    &lt;/template>
    &lt;template if="{{!responsive}}"> &lt;!-- Non-responsive case -->
     ...
    &lt;/template>
  &lt;/template>
  &lt;script>Polymer('responsive-layout', {responsive: false});&lt;/script>
&lt;/polymer-element>
</pre>

<pre class="prettyprint" data-lang="User's HTML">
&lt;responsive-layout <b>responsive</b>>
  &lt;div>...&lt;/div>
&lt;/responsive-layout>
</pre>

---

hidden: true
id: the-platform
title: The <label class="platform">platform</label>
subtitle: <a href="http://www.polymer-project.org/docs/start/platform.html" class="nounderline">polymer-project.org/docs/start/platform</a>
class: nobackdrop nobackground segue platform polymer-diagram
#content_class: flexbox vcenter
keep_content: true

<div id="blocks-3d" class="in" style="top: 10%;">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

---

hidden: true
body_class: platform-fill
content_class: flexbox vleft

<h2 class="faded" style="font-size: 54px;">The platform is a <em>layer of polyfills</em> that adds support for emerging standards, like <em>Web Components</em>, to all <em>modern browsers</em>.</h2>

---

hidden: true
id: platform-polyfills
title: Platform polyfills
subtitle: supporting new web technologies today
class: nobackdrop nobackground browser-support

<div class="flexbox">
  <h2>Templates</h2>
  <div class="browser-support-row">
    <div class="supported"><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>HTML Imports</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported partial"><img src="images/logos/chrome_logo.png"></div>
    <div><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>Custom Elements</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported partial"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>Shadow DOM</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported partial"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="build">
  <span id="polyfill-support-all"></span>
</div>

---

hidden: true
body_class: platform-fill
content_class: flexbox vleft

<h2 class="faded" style="font-size: 52px;">Additional features include <em>Mutation Observers</em>, <em>Pointer Events</em>, <em>Web Animations</em>, and much more.</h2>

---

body_class: iceberg
body_overlay: light-black
class: nobackground nopadding
content_class: flexbox vcenter

<h2 style="color: white; font-size: 60px;">Changing Our Process</h2>

---

body_class: flowers2
body_overlay: core
class: nobackground nopadding fill
content_class: flexbox vcenter

<h2 class="faded"><em>Living</em> Style Guides</h2>

---

body_class: tracks
body_overlay: elements
class: nobackground nopadding fill
content_class: flexbox vcenter

<h2 class="faded">Build <em>Prototypes</em></h2>

---

id: polymerurl
class: nobackdrop nobackground yum do-transition
content_class: flexbox vcenter centered

<div class="build">
<h2><a href="http://polymer-project.org"><span class="elements">polymer</span><span class="hide">-</span><span class="core">project</span><span class="hide">.</span><span class="platform">org</span></a></h2>
</div>
