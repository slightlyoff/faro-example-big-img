---
class: "intro"
eleventyComputed:
  title: "{{ talk.talkTitle }}"
  date: "{{ talk.eventDate }}"
build: false
---
{# {{ title | debug }} #}
<div class="contact">
  {{ talk.speaker.name }} <br>
  {{ talk.speaker.url | urltext }} <br>
  {{ talk.speaker.email }} {% fa "envelope" %} <br>
  {{ talk.event }} &mdash; {{ talk.eventDate | longdate }}<br>
</div>

<!-- --- -->
---
title: "Slide 2"
subtitle: "Stuff to say"
# Animations in the box: wipe, wipe-v, wipe-tilt, wipe-iris, wipe-hard, zoom
animation: wipe
# Build can be "all" or "true"; "all" reveals lists per bullet
build: false
---

 - You can use Markdown _here_.
 - [Links work!](https://wikipedia.org)
 - **Iguanas look cute in hats**. `[ citation needed ]`

{% notes %}
Here are some notes!

You can use *Markdown*, including [links](https://infrequently.org)
{% endnotes %}


<!-- --- -->
# Slide 3
## You Can Use Regular Titles Too

Frontmatter _optional!_ Dare to:

 - Use a plain `#` for title
 - Drop in a `##` for the subtitle
 - Avoid shortcodes!
<!-- --- -->
---
layout: big-img
# imgUrl, or imgId
img: unsplash:MAYsdoYpGuk
creditClass: lighter
---
<!-- --- -->
---
layout: big-img
img: flickr:32412942596
creditClass: darker
title: "Oh Hai."
subtitle: "What ho!"
class: dark glass
skipFirst: 1
animation: wipe-tilt
---
<!-- --- -->
---
build: content
class: dark
---
# Is That...Code?
{% code lang="js", 
        lineNumbers=false, 
        buildSet="0,1-5,7-*" -%}
class Foo extends Bar {
  constructor() {
    console.log(
      "my kingdom for fatty structs!"
    );
  }
}

let f = new Foo();
{%- endcode %}
<style>
  /* TODO: extract to a code slide style */
  f-slide {
    background: #1a1b26;

    h1 {
      margin-bottom: 1rem;
    }
    code {
      font-size: var(--smaller);
      line-height: 1.0;
    }
    micro-lighter::part(line-numbers),
    faro-lighter::part(line-numbers) {
      font-size: calc(var(--smaller) * 0.8);
      border-right: 1px solid var(--syntax-comment);
      margin-right: 1rem;
    }
  }
</style>
{#
{% code lang="md", lineNumbers=false %}
# A Title
## ...And A Subtitle

  - And a list
  - With stuff

And _italics._
{% endcode %}
#}
<!-- --- -->
---
layout: big-img
img: flickr:32331836541
creditClass: light
class: dark glass
skipFirst: 1
---
# Here's An Inline Title { .whatevs }
## ...and a subtitle { .blarg .stuff }
<!-- --- -->
---
layout: big-img
img: https://unsplash.com/photos/blue-circuit-board-jXd2FSvcRr8 
creditClass: light
---
<!-- --- -->
---
layout: big-img
img: flickr:31641199803
creditClass: lighter
animation: wipe
---
<!-- --- -->
---
layout: big-img
img: wiki:LondonScienceMuseumsReplicaDifferenceEngine.jpg
creditClass: light
animation: zoom
---
<!-- --- -->
---
layout: big-img
img: wiki:File:Cat_(2188027041).jpg
creditClass: lighter
animation: zoom
---
<!-- --- -->
---
layout: big-img
img: raw:./talk/assets/images/PXL_20260906_095000995.jpg
credit:
  name: "Alex Russell"
  url: infrequently.org
  class: lighter
animation: horizontal
---
{#
<!-- --- -->
---
layout: big-img
img: PXL_20260905_124518945.jpg
credit:
  name: "Alex Russell"
  url: infrequently.org
  class: darker
---
#}
<!-- --- -->
---
layout: big-img
img: PXL_20260904_132931403
credit:
  name: "Alex Russell"
  url: infrequently.org
  class: lighter
animation: vertical
---
<!-- --- -->
---
layout: big-img
img: PXL_20260905_124519587
credit:
  name: "Alex Russell"
  url: infrequently.org
  class: lighter
animation: vertical
---
<!-- --- -->
---
layout: big-img
img: talk/assets/images/PXL_20260909_210644831.jpg
animation: horizontal-bounce
credit:
  name: "Alex Russell"
  class: lighter
  url: infrequently.org
---
<style>
  .big-img {
    background-color: #111418;
    background-size: contain;
  }
</style>
<!-- --- -->
---
layout: big-img
img: flickr:33433414158
creditClass: lighter
animation: horizontal-bounce
---
<style>.big-img { background-size: cover; }</style>
<!-- --- -->
---
class: dark
animation: vertical-bounce
---
# Get In Touch With The Dark Slide
<!-- --- -->
---
title: "Thank You All"
class: "outro"
build: false
---
<div class="contact">
  {{ talk.speaker.name }} <br>
  {{ talk.speaker.url | urltext }} <br>
  {{ talk.speaker.email }} {% fa "envelope" %} <br>
  {{ talk.speaker.mastodon | urltext }} {% fa "mastodon" %} <br>
  {{ talk.speaker.linkedin | urltext }} {% fa "linkedin" %} <br>
  {{ talk.speaker.bsky     | urltext }} {% fa "bluesky" %} <br>
</div>