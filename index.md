---
layout: default
---

<div class="card" markdown="1">

# Scouting the Web since 2012

The world is wonderful. So many places for the mind to wander. So many ideas to explore. There lives such an amount of
knowledge, passion, ideas on this planet. A portion of which ends up on the Internet and will get discovered, shared and
improved. This website is my curated trove of discoveries. Articles, snippets, ideas and more.

Sometimes, 280 characters don't bring enough context. Explaining why content deserves attention takes longer. It may
be because it deals with a topic of importance to me or because it demonstrates progress, some vision years in the
making, years into the future. The future we are building, one idea at a time.

**The FollowUp** sits there.

Do not forget to [leave some feedback](https://vcz.fr/apps/feedback/?appid=hS7YejNaDu6k) so that I can make your
experience better.

Back to you now!

</div>

{% assign latest = site.posts | slice: 0, 10 %}
<div class="card" markdown="1">

## Latest posts

{% for post in latest -%}
1. [{{ post.title }}]({{ post.url }}) sent {{ post.date | date: "%A %B %d, %Y" }} in [{{ post.categories.first }}](/categories/{{ post.categories.first | slugify }})
{% endfor %}

_Discover [{{ site.posts.size | minus: 10 }} more posts](/all)&hellip;_

</div>