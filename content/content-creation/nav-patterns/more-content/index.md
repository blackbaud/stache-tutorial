---
layout: layout-container
name: More Content!
description: More advanced content creation.
data:
  - name: Brandon
  - name: Steve
  - name: Bobby
order: 2
icon: plus
---

# More Content!

## Images

<p>
  <h3>HTML</h3>
  <img src="../../../assets/img/githubrocket.png">
  <p>`<img src="../../../assets/img/githubrocket.png">`</p>
</p>

<a href="{{ stache.config.nav_patterns }}">Nav patterns</a>


### Markdown
![Github Rocket](../../../assets/img/githubrocket.png)

`![Github Rocket](../../../assets/img/githubrocket.png)`


## Links

<p>
  <h3>HTML</h3>
  <a href="{{ stache.config.base }}">Home</a>
  <p ng-non-bindable>`<a href="\{{ stache.config.base }}">Home</a>`</p>
</p>

### Markdown
<div ng-non-bindable>

[Home]({{ stache.config.base }})

`[Home](\{{ stache.config.base }})`

</div>
## Code Samples

<pre><code class="language-javascript">/*global angular */

(function () {
    'use strict';

    function CarouselTestController() {
        var i,
            itemCount = 20,
            vm = this;

        vm.items = [];

        for (i = 0; i < itemCount; i++) {
            vm.items.push(i + 1);
        }
    }

    angular.module('stache')
        .controller('CarouselTestController', CarouselTestController);
}());</code></pre>

## Data

### Yaml

<pre ng-non-bindable><code class="language-yaml" ng-non-bindable>---
layout: layout-container
name: More Content!
description: More advanced content creation.
data:
  - name: Brandon
  - name: Steve
  - name: Bobby
---
&lt;ul&gt;
\{{# each data }}
  &lt;li&gt;\{{ name }}&lt;/li&gt;
\{{/ each }}
&lt;/ul&gt;
</code></pre>

<ul>
  {{# each data }}
  <li>{{ name }}</li>
  {{/ each }}
</ul>

### JSON

<pre ng-non-bindable><code ng-non-bindable>{
  "example": [
    {
     "title": "JSON",
      "sample": "This is some text.",
      "example": "This is an example.",
      "link": "http://www.google.com"
    }
  ]
}

&lt;h3&gt;\{{ sample.example.0.title }}&lt;/h3&gt;
&lt;p&gt;\{{ sample.example.0.sample }}&lt;/p&gt;
&lt;p&gt;&lt;a href="\{{sample.example.0.link}}"&gt;Link&lt;/a&gt;&lt;/p&gt;</code></pre>

<h3>{{ sample.example.0.title }}</h3>
<p>{{ sample.example.0.sample }}</p>
<p><a href="{{sample.example.0.link}}">Link</a></p>

## Includes

<pre><code ng-non-bindable>## Example!

This is some reusable content. You would definitely want to use this in more than one place.

\{{ include 'includes/include-example.md' }}</code></pre>

{{ include 'includes/include-example.md' }}
