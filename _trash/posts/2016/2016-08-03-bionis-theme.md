---
title: "Introducing the 'Bionis' theme"
date: 2016-08-03
excerpt: "This is a major redesign of my website. Makes content look like raw markdown. Uses a new colour scheme."
permalink: /bionis-theme/
---
I redesigned my website with the intention to pursue a couple of objectives:

- review and clean up the site's source code;
- deliver a style that reflects my recent career reorientation towards front end development.[^CareerChangeNote]

The *Bionis* theme is my take on an older idea: to make styled HTML look like raw Markdown. I wanted to try this ever since I first started writing in plain text. But with my target audience at the time being non-developers, I opted for the more familiar feel of [Akademos](/akademos/), my previous theme.

The emulation of the plain text markup is not absolute. Certain typographic norms not present in generic text editors are implemented herein. For instance, a subheading's margin is higher on top and lower on the bottom, while a universal type scale is applied.[^TypescaleNote]

## Evolution, not revolution

While the redesign may seem quite radical, it is not meant to break any of my older theme's features. A degree of continuity is necessary, lest we end up having to rework older pages whose content remains relevant.

This is where the modularity of Sass comes in handy.[^SiteSourceCode] A new `_markdown.scss` determines the look of the article's content, while the rest of the stylesheet remains constant (more or less).

Writing modular styles is both efficient and future-proof. Ideally, ad hoc solutions are avoided, though I admit they sometimes are the most practical course of action.

As a website grows, so do its needs. New content may be introduced that makes use of novel components to present information. A case in point are my [Prot16](/schemes/) project pages. Items such as the 'packages' module or the palette are specific to them.

Sass partials can help manage the influx of originally unforeseen content, incorporate it in the greater whole, yet still keep it in a quasi self-contained state.

## The case of the menubar

The 'menubar' is the column that includes links to the homepage, my profile, contact info, blog, social media, etc. On desktops it will appear as a fixed sidebar to the left of the main content area. Mobiles and tablets will show it at the top of the viewport as a typical masthead. In this section I will be referring to the desktop view.

Perhaps counter-intuitively, two-or-more-column blogs are not my favourites. Supplementary information tends to be excessive and distracting. The problem is compounded by the presence of text- or graphics- heavy headers and footers. Whereas single column designs focus on what matters the most: *the article*.

The major drawback of single column designs is a sort of disconnect they create between the *content* and its *context*. By the time the average user is done scrolling to the end of the post, they have forgotten all about checking out the rest of the page. I do that all the time. And I tend to completely disregard a website's peculiar character the more generic or "minimalist" it tries to be (I am a proponent of minimalism, though not of the misguided tendency to homogenise everything).

To make site navigation more immediate without rendering it intrusive, I settled on a couple of principles:

1. **Block-level contrast.** To enhance the presentation of the content area, the menubar would have to use the colour scheme's dark variant, which is easy given the palette of all Prot16 projects.
2. **Reading rythm prioritisation**. The menubar's content would be situated at the bottom of the screen and be kept small in size, guiding the eye towards the top of the page and slightly to the right where the body of text is located.

Based on the admittedly limited user testing I conducted, the first thing a visitor will notice is the content area. It is brighter and more colourful. Also, in English we read from top to bottom and from left to right. It is second nature. By following that pattern, we encounter the page's `h1` heading before anything else.

These contribute to the two-fold goal of (i) focusing on the content, without (ii) neglecting the context.

## Next up

Bionis may still undergo some minor refinements. Once I am completely satisfied with the end product, I will package it as a Ruby gem so that it may be easily installed on any other Jekyll-powered site. A provisional date is late 2016. That is when I expect to also release Akademos.

More on these plans when the time nears. Until then, I hope you enjoy the reading experience on protesilaos.com and appreciate the new theme for what it is trying to achieve.

By the by, the term 'Bionis' also denotes a colour scheme that was produced in tandem with—and specifically for—the needs of this new design. It follows the guidelines of Prot16, which suggests that it will eventually be developed as a syntax theme for the Atom text editor and related apps.

[^CareerChangeNote]: I used to be a policy analyst. For context, [read the announcement](/diary/new-career/).

[^TypescaleNote]: The type scale is the [minor second](http://www.modularscale.com/).

[^SiteSourceCode]: This site is built with Jekyll. On GitHub you may find [its source code](https://github.com/protesilaos/protesilaos.github.io).
