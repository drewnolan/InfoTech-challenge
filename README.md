# InfoTech-challenge
I received this [challenge problem from InfoTech](original/Frontend%20Developer-Take%20Home%20Challenge%20(1).pdf).

It originally [looked like this](https://htmlpreview.github.io/?https://github.com/drewnolan/InfoTech-challenge/blob/main/original/index%20(6)%20(1).html).

[I did this.](https://htmlpreview.github.io/?https://github.com/drewnolan/InfoTech-challenge/blob/main/index.html)

  * [Plan](#plan)
  * [Tasks](#tasks)
  * [Miscellaneous Notes](#miscellaneous-notes)
    + [How long did this take?](#how-long-did-this-take)
    + [Why no javascript?](#why-no-javascript)
    + [Will this work on IE?](#will-this-work-on-ie)
    + [Why did you leave out the `--moz*` and `--webkit*` properties?](#why-did-you-leave-out-the---moz-and---webkit-properties)
    + [How did you derive screen widths 600 and 1024 as media query cutoffs?](#how-did-you-derive-screen-widths-600-and-1024-as-media-query-cutoffs)
    + [What's with shoving the images into CSS?](#whats-with-shoving-the-images-into-css)
    + [Use of `doc-subtitle` in feed motto 'Always Be Closing'](#use-of-doc-subtitle-in-feed-motto-always-be-closing)
  * [Things I would do if I had more time or an API or a Framework](#things-i-would-do-if-i-had-more-time-or-an-api-or-a-framework)
    + [Light Mode](#light-mode)
    + [Make the dropdown for leaderboard do something](#make-the-dropdown-for-leaderboard-do-something)
    + [Table sorting](#table-sorting)
    + [Profile modal](#profile-modal)
    + [Chat](#chat)
    + [Analytics](#analytics)
    + [Make the responsiveness better at extremely large and small sizes](#make-the-responsiveness-better-at-extremely-large-and-small-sizes)
    + [Test with a screen reader](#test-with-a-screen-reader)

## Plan

* User Story: "As an executive, I want to understand how salespeople are performing at a glance"
* Return a single HTML file
* Fix any issues with the HTML
* Add semantic markup
* Make the UI responsive
* Run some validators against the file
* Have a little fun

## Tasks
I kept track of the tasks I did while working on this [if you are interested](doc/tasks.md)

## Miscellaneous Notes

### How long did this take?
Yes, I spent more than the estimated time.  Part of that is I saw it as an opportunity to try `grid`, which I have never had the opportunity to use at this level.  Also, I usually do not get the time to really dive into the trivia around semantic choices.

Another part is I am hoping to impress.  Also, I find this kind of coding fun, and I do not get to do it framework free like this a lot.

### Why no javascript?
I use javascript (ES6+ mostly) about 90% of the time in my current job.  I thought it would be interesting to use CSS and HTML only.  Plus this is a static HTML file, so not much interesting to do.

If needed, I am happy to be quizzed on javascript anytime.

### Will this work on IE?
Nope.  I used custom properties, for one thing.  If I was using SASS or an equivalent tool, then it would probably be more backward compatible.

There are other modern features I used, though I did test with Firefox and Chrome and my Android phone

### Why did you leave out the `--moz*` and `--webkit*` properties?
This is a fairly mechanical process, and so I skipped it to make time.

### How did you derive screen widths 600 and 1024 as media query cutoffs?
part because I was using a 1->2->4 column progression and part via trial and error.

### What's with shoving the images into CSS?
Since these are really avatars, they do not really add a lot to the screen reader beyond the name.  Moving them to CSS takes them out of the semantic content.

### Use of `doc-subtitle` in feed motto 'Always Be Closing'
I thought about this for a while, and it sees legit since I am targeting screen readers.  Note caveats here https://adrianroselli.com/2020/08/be-wary-of-doc-subtitle.html

## Things I would do if I had more time or an API or a Framework

### Light Mode
I snagged a dark color scheme from a color scheme site.  I would have liked to make a switch to go to light mode, but not enough time.

### Make the dropdown for leaderboard do something
This would just be rewriting the leaderboard in `onchange`.  Trivial in a framework.  Not hard if I moved the data into JSON.

### Table sorting
This would have not been hard had I moved the data into JSON, however, it seemed like more than I wanted to tackle

### Profile modal
Could have used the `expand` stuff in ARIA to do this accessibly, but I am not personally crazy about modals and I would have duplicated a chunk of HTML modal code for each sales team member.  This would be a lot easier with a framework

### Chat
Emulating a little chat box is also not terribly hard, but With that kind of thing I would really want to work with an existing package.

### Analytics
I would love to spy on you using this, but, alas, Google Analytics does not support `file:` URLs that I can see.

### Make the responsiveness better at extremely large and small sizes
Probably just add an expanding side margin at large sizes and some min sizes with scroll for small.

### Test with a screen reader
