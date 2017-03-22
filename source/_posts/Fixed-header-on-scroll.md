---
title: "How to create: Fixed header on scroll."
excerpt: "An example on how to create a fixed header on scroll. I needed to created a fixed header but only after the user has scrolled down a specific point. I couldn't find any examples so I built my own."
date: 2013-05-31
tags: [css, javascript, jquery, pre-work, api]
comments: true
---
I had a project at work that one of the designers wanted to load search results(Conference Rooms) below a search bar. As the user scrolled down the label "Results" would stay at the top of the screen. This was inspired by the phone scrolling that many of us see as we scroll down our contact lists on iPhone, windows or android devices.

I found plenty of examples on how to do a fixed header on page load, but very few examples of how to incorporate a fixed header once the user scrolled past a certain point. After an "aha" moment while taking a walk around the office park I thought their must be some way to track the scroll position using JavaScript and then use a conditional to display the fixed header when appropriate.

Below was the completed code needed.
{% codeblock javascript %}
// Show / Hide fixed label on scroll
	$('.toolbar').scroll(function (e) {
    //console.info(e.currentTarget.scrollTop);
		if (e.currentTarget.scrollTop >= 130) {
			$('.results-label').addClass('fixedSimilarLabel');
		}
		else {		
			$('.results-label').removeClass('fixedSimilarLabel');
		}
	});
{% endcodeblock %}
I found out about [jQuery scroll function](https://api.jquery.com/scroll/){:target="_blank"} and tracked the event as I scrolled using <code>console.log</code>, which then led me to <code>e.CurrentTarget.</code>[ScrollTop](https://api.jquery.com/scrollTop/){:target="_blank"} to get the current vertical position of the scroll bar for the element.

<figure>
    <a href="/images/e.currentTarget.PNG"><img src="/images/e.currentTarget.PNG"></a>
    <figcaption>Moving down the event to find currentTarget and finally ScrollTop</figcaption>
</figure>

The next step was to create a conditional based on where the scroll bar was. If it scrolled past where I wanted to I would use the [addClass()](https://api.jquery.com/addclass/){:target="_blank"} and [removeClass()](https://api.jquery.com/removeclass/){:target="_blank"} functions. Its not super important how you style it, ust that you put <code>position:fixed</code> and it looks as seemless as possible when you scroll down. You can edit the left and right values as well as the width to make it work for your requirements.
<figure>
    <a href="/images/fixedcss.PNG"><img src="/images/fixedcss.PNG"></a>
    <figcaption>My styles for the fixed label</figcaption>
</figure>
<p data-height="500" data-theme-id="0" data-slug-hash="pjEzeK" data-default-tab="result" data-user="franklynroth" class='codepen'>See the Pen <a href='http://codepen.io/franklynroth/pen/pjEzeK/'>Sticky Header on Scroll</a> by Franklyn (<a href='http://codepen.io/franklynroth'>@franklynroth</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Of course once I thought of the solution and built it. I was able to find many more examples. [scroll-fix-content](https://css-tricks.com/scroll-fix-content/){:target="_blank"}, [sticky-header-after-scrolling-down](http://stackoverflow.com/questions/18382496/sticky-header-after-scrolling-down){:target="_blank"}, [sticky-header-after-some-scrolling](http://stackoverflow.com/questions/24545052/sticky-header-after-some-scrolling){:target="_blank"}
Either way, I learned a lot by figuring out how to build this myself. Hope this code helps.
