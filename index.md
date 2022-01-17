---
layout: default
---

<div class="card">
{%- capture text -%}

# For when a tweet is just not enough

Hello, Vincenzo **Scalzi** here!

The world is wonderful. So many places for your mind to wander around. So many ideas to explore. So many thoughts to
traverse one's head. We are billions and we produce such an amount of knowledge, passion, ideas. A portion of which ends
up on the Internet and will get discovered, shared and improved upon. This website aims to become my own curated trove
of discoveries. Articles, snippets, ideas and much more.

At times, [140 or 280 characters](https://twitter.com/vcz_fr){:rel="nofollow"} bring just not enough context. Explaining
why a content deserves your attention can take longer. It may be because it deals with a topic I am attached to or
because it demonstrates progress, a vision years in the making, years into the future. The future we are building, one
idea at a time.

Introducing **The FollowUp** with an age-old pledge: a fast and reliable experience with no tracking on my side. Ever.

As for this site, it is open source, hosted and delivered by [Cloudflare](https://www.cloudflare.com/){:rel="nofollow"}
and uses [Jekyll](https://jekyllrb.com/){:rel="nofollow"} to generate content.

There is no server to manage, no hosting costs or headaches, just a domain. Just a domain with free content you will
appreciate. I can only hope you will like it as I will never add any third party comment tool or analytics. If you do
enjoy the contents, come by [the place that hosts it](https://github.com/vcz-fr/TheFollowup){:rel="nofollow"} and leave
your mark. Or check out my [personal website](https://vcz.fr), my [Meetup notes](https://meetups.vcz.fr), my [blog](https://blog.vcz.fr)
or my [apps](https://apps.vcz.fr).

Do not forget to [leave some feedback](https://apps.vcz.fr/app/feedback/?appid=hS7YejNaDu6k) so that I can make your
experience better.

Back to you now!

{%- endcapture -%}
{{ text | markdownify }}
</div>

{% assign latest = site.posts | slice: 0, 10 %}
<div class="card">
{%- capture text -%}
## Latest posts

{% for post in latest -%}
1. [{{ post.title }}]({{ post.url }}) sent {{ post.date | date: "%A %B %d, %Y" }} in [{{ post.categories.first }}](/categories/{{ post.categories.first | slugify }})
{% endfor %}

_Discover [{{ site.posts.size | minus: 10 }} more posts](/all)&hellip;_

{%- endcapture -%}
{{ text | markdownify }}
</div>