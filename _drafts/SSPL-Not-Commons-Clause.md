---
title: SSPL Is Not Commons Clause
description: how open licensing blew its biggest opportunity of the 2010s
layout: post
---

<aside class="brief" markdown="1">
I summarize the missed opportunity that was MongoDB's Server Side Public License, and how it was missed.
</aside>

MongoDB's [Server Side Public License][SSPL] is fundamentally different from [Commons Clause].  Inability and simple unwillingness to express and recognize that fact squandered a once-a-decade opportunity for open source as a community of practice.  The ensuing spat and fractious, walk-away ceasefire instead make everyone involved---the companies, the pundits, the Open Source Initiative, the lawyers---look petty, blinkered, selfish, and incompetent, from nearly any outside point of view.

We deserve it.

## WTF was Commons Clause?

In general, permissive open source licenses like [MIT], [BSD], and [Apache] say:

```
Do what you want with this software.
```

[Apache]: https://spdx.org/licenses/Apache-2.0.html

[BSD]: https://spdx.org/licenses/BSD-2-Clause.html

[Commons Clause]: https://commonsclause.com/

[MIT]: https://spdx.org/licenses/MIT.html

[GPL]: https://spdx.org/licenses/GPL-3.0.html

Copyleft licenses like [MPL], [GPL], and [AGPL] say:

```
Do what you want with this software.

Share improvements and extensions you make alike.
```

[Commons Clause] is a bolt-on "patch" to any open source license, permissive or copyleft.  Highly oversimplifying yet again, Commons Clause appends:

```diff
+ But don't use it to compete with its developer.
```

So "MIT with Commons Clause" says:

```diff
  Do what you want with this software.
+
+ But don't use it to compete with its developer.
```

And "AGPLv3 with Commons Clause" says:

```diff
  Do what you want with this software.

  Share improvements and extensions you make alike.
+
+ But don't use it to compete with its developer.
```

Companies that wanted "but don't compete" used different open source licenses.  Some chose permissive, especially [Apache].  Others chose copyleft, especially [AGPL].

Writing Commons Clause as a generic patch enabled all of those companies to adopt one new text, Commons Clause, instead of a whole slate of new licenses, from permissive to weak and strong copyleft, corresponding to MIT with Commons Clause, Apache with Commons Clause, AGPL with Commons Clause, and so on.  On the user side, those accustomed to MIT and Apache and AGPL on the receiving end could apply what they already knew about those licenses, and simply tack on the Commons Clause question: Are we competing with the developer?

But regardless of which open source license the companies started with, adding Commons Clause violated general principles associated with "open source".  Again seriously overgeneralizing, I'd guess most developers today understand open source as follows:

> I can do what I want with open source that I find.  There's just one catch: Copyleft, like GPL, requires sharing back.  As long as I avoid copyleft, I can do what I want.

Commons Clause says you can't do what you want if that happens to be using the software to compete against its developer.

Even if the vast majority of developers looking at a database under Commons Clause want to make applications, not compete in the database market, "Do what you want." is no longer absolute under Commons Clause, and it doesn't feel right to call Commons Clause software open source.  So the companies adopting it did not.

## Ick

The companies and lawyers behind Commons Clause understood that it was not open source in principle.  I strongly suspect they didn't feel the best about that, either.

Many of these companies seem to have released open source early on not because they saw it as a surefire path to business glory, but because they liked and identified with open source, wanted to contribute back, and hoped to build companies appreciated for doing so.  It is far, far easier to convince a professional investor to sign off on a restricted license than some mishmash of old open source license and new bolt-on clause, to take a "secret sauce" approach to everything.  They didn't do that.

But they felt threatened by Amazon and other cloud providers, not just directly, but in terms of the longer-term story they could tell investors and their people.  None of them had much individual leverage against that kind of dominant player.  The best they could do was band together under a [sympathizing, if unsympathetic, venture capitalist](https://techcrunch.com/author/salil-deshpande/), pool resources, and hire [Heather Meeker](https://heathermeeker.com) to write one set of terms they could use to mount a common defense.  So they did.

## Tea Leaves

I read and write licenses all the time.  My first impression of Commons Clause's text was that it merely _transcribed_ companies' description of the behavior they wanted to stop, and prohibited it.  Commons Claus _translated_ that rule into legal terms only to the minimum extent absolutely necessary.  The result reads like a snippet of commercial software license, not a snippet of open source license, and not a snippet of the [more progressive drafting work](https://fair.io/) [work](https://polyformproject.org/) Heather's been a part of before and since.

Straight out of Commons Clause:

> Without limiting other conditions in the License, the grant of rights under the License will not include, and the License does not grant to you, the right to Sell the Software.

Translation:  This is a patch.  The only thing it's changing is taking away one right, the right to sell the software, as we're about to define "sell".  Everything else that out open source license lets you do, you can still do.

Then:

> ... "Sell" means practicing any or all of the rights granted to you under the License to provide to third parties, for a fee or other consideration (including without limitation fees for hosting or consulting/support services related to the Software), a product or service whose value derives, entirely or substantially, from the functionality of the Software.

Translation:  "Sell" means doing anything with this software in order to sell others products or services that are mostly just this software.

This is where Commons Clause attempts to draw the line between applications, which all these companies want others to build for free, and competitive offerings, which they want to prohibit.

To make that concrete:  As a database company, I might be fine with others building inventory management, social media, and other applications using my database as data store, absolutely free.  After all, I might get to sell them training or support or database hosting down the line.  But I don't want others selling a competitive version of my database with patches they refuse to share back, or crushing me in the database-as-a-service business because they'd already run away with that game before I started playing.

## SSPL

My first impression of MongoDB's Server Side Public License was that Heather wrote it.  I know my kind.

My second impression was that somebody made her cram Commons Clause into AGPL.  SSPL didn't seem to _translate_ Commons Clause into open licensing terms so much as _transplant_ it into AGPL, an existing open license.

Those impressions aren't great, and both Mongo and Heather could have done far better.  But in the end, that's all surface.  In style, SSPL's section 13 reads like commercial license language.  It tracks the business way of expressing its objective.  But the underlying mechanism that language invokes, copyleft, is at the core of free and open licensing.

The effect is a bit like a Ruby or Python wrapper around a C library.  At first glance, it's just more Ruby or Python.  You have to look deeper to see that it's invoking something different in kind.

SSPL _doesn't_ say:

> Don't use MongoDB to compete with MongoDB, Inc.

Rather, SSPL says:

> Share improvements, extensions, and code you use to provide MongoDB services alike, but do what you like with applications built on top.

That general thrust isn't new.  A whole class of broadly accepted free and open software licenses, called "weak copyleft" licenses, have much the same effect.  On the surface, however, existing weak-copyleft licenses tend to express their rules in open-speak or developer-speak, rather than business-speak.  You have to work SSPL and the old weak-copyleft licenses in context to see their resemblance.

Consider [LGPL], [MPL], and [EPL].  Each requires sharing changes, extensions, and other work on the licensed software itself, but not larger programs built with that software.  In general, if you patch a weak-copyleft library and share a copy with someone else, you have to share your patch alike.  But if you build a program using that weak-copyleft library, you don't have to share your whole program alike.

If MongoDB wanted improvements to MongoDB-as-software and MongoDB-as-a-service shared back, but not applications built with MongoDB, why didn't they just take a weak-copyleft license off the shelf?

Visually:

|             | Patches | Extensions | Wrappers          | Applications      |
|-------------|---------|------------|-------------------|-------------------|
| **[LGPL]**  | Share   | Share      | Keep              | Keep              |
| **[MPL]**   | Share   | Share      | Keep              | Keep              |
| **[EPL]**   | Share   | Share      | Keep              | Keep              |
| **[AGPL]**  | Share   | Share      | It's complicated. | It's complicated. |
| **[SSPL]**  | Share   | Share      | _Share_           | _Share_           |

[AGPL]: https://spdx.org/licenses/AGPL-3.0.html
[EPL]: https://spdx.org/licenses/EPL-2.0.html
[LGPL]: https://spdx.org/licenses/LGPL-3.0.html
[MPL]: https://spdx.org/licenses/MPL-2.0.html
[SSPL]: https://lists.opensource.org/pipermail/license-review_lists.opensource.org/2018-November/003836.html

None of the old weak-copyleft licenses requires sharing back improvements to the software that take the form of wrappers like monitoring, orchestration, and backup code, rather than patches to existing source code.  All the old weak-copyleft licenses treat wrappers like applications exempt from copyleft, not patches or extensions that have to be shared alike.  Worse yet, it's often simply unclear.  All those licenses were written before service composition became a widespread approach in mainstream software development.  They all pretty much assumed that big programs get built out of smaller programs by linking them together.

MongoDB's lawyer, Eliot Horowitz, called this out right at the top of [his rationale for proposing SSPL](http://lists.opensource.org/pipermail/license-review_lists.opensource.org/2018-October/003603.html) to the Open Source Initiative for review:

> Today, Affero GPL 3.0 uses the broadest scope of copyleft, among the commonly used open source licenses. ...
>
> The Remote Network Interaction provision of AGPL has not provided enough incentive to change the behavior of cloud providers for several reasons:
>
> - It is not clear that it extends to software that controls the functionality of the database software, such as management, automation, monitoring, storage and hosting software.
>
> - It only applies if the software is modified, and the definition of a modification references back to copyright principles that are not settled law.

In his [later response to comments](http://lists.opensource.org/pipermail/license-review_lists.opensource.org/2018-October/003672.html), Eliot made the historical argument, as well:

> [I]f I have an AGPL key value store library and I combine it with a network library and a management UI, then the copyleft provisions of the AGPL apply to this use of the network library and the management UI, because of linkage.  However, if someone splits out the management UI to a separate component that only interacts with the combined key-value store and network library over a socket or other IPC mechanism, it is unclear whether existing licenses' copyleft provisions apply to that split-out management UI.  For a program that is used only as a network service, we want to be sure that all components that make up the service, e.g. management and backup, are included in the scope copyleft provision of the SSPL.
>
> In short, we believe that in today's world, linking has been superseded by the provision of programs as services and the connection of programs over networks as the main form of program combination.  It is unclear whether existing copyleft licenses clearly apply to this form of program combination, and we intend the SSPL to be an option for developers to address this uncertainty.

MongoDB was well aware that Commons Clause could address that uncertainty.  But rather than saying "Don't use MongoDB to compete with MongoDB, Inc.", parting ways with open source principle and shutting the door on potential collaboration, MongoDB preferred to say "Share the code you use to provide MongoDB services alike.", through copyleft, and leave the door open.  Pulling again from Eliot's original submission statement:

> However, for some kinds of software that is popular for cloud deployment, AGPL has not resulted in sufficient legal incentives for some of the largest users of infrastructure software, such as international cloud providers, to participate in the community.   Many open source developers are struggling with a similar reality, and some of our competitors have moved to proprietary licensing models [e.g. Apache 2.0 with Commons Clause ---KEM].  The alternative, to be blunt, is for us to be that last standing unpaid open source database developer for cloud providers, who sell access to our software for significant fees, but may not adequately contribute back to our community.  Faced with the choice of moving to a proprietary model by applying licensing restrictions [e.g. Commons Clause ---KEM] to our software, we prefer instead to continue using the copyleft model to create a workable incentive for cloud providers to share with the rest of the community.

This was MongoDB offering to compromise, and seeking guidance on how to implement that compromise, as a kind of copyleft.  The most direct, reliable, and clear way to meet MongoDB's business need was just to describe the competitive behavior they wanted to stop, in business terms, and drop it into a flat-out restriction on use of its database, like Commons Clause.  Rather than do that, MongoDB attempted to write a copyleft rule that achieves the same effect at least some of the time.

Some of the time.  Compared to a flat-out restriction, copyleft inherently gives ground.  License restrictions say "Thou shalt not."  Copyleft says "If thou dost, share thy work alike."  Nobody really expects AWS to share all its wrapper code around a database.  But someone else might.

From the business perspective, copyleft leaves open the possibility that someone will come along, use your code, honor your requirement to share alike, and still outcompete you.  From MongoDB's point of view, offering SSPL-style copyleft terms is taking a bet that another company can't outcompete them while also sharing the kind of hosting code that MongoDB keeps to itself.

That speaks directly to MongoDB's history.  MongoDB, Inc. began as 10gen, a startup attempting to offer a fully open source cloud.   In time, they pivoted to focus on the first component of that cloud platform, a database, and renamed their company to suit.  In short, MongoDB wanted to be "open source AWS", but open-sourced its S3, rather than keeping it closed, and morphed into the commercial force behind that project.  They did well from seed stage to growth, and eventually went public.  Now MongoDB has chosen a license for its database, SSPL, that would allow the company it originally wanted to be, 10gen, to directly compete with their hosted offerings.

To put it another way, from the outside point of view: SSPL-style copyleft terms put a bounty on the business model that 10gen tried and failed to find.  If you find a way to beat MongoDB, Inc. while sharing all the code you use to do so, you're welcome to MongoDB, gratis.  If you find a way to be open source AWS, you can offer MongoDB as a part of that platform, without cutting any special deal.

## Old Hat

SSPL represents exactly the same kind of dare that companies have long made for other kinds of software, under old copyleft licenses, weak and strong, that reached all relevant code.

When companies develop software components that were already common twenty years ago, like C libraries used in embedded devices, the copyleft licenses of that era accomplish the same business effect that MongoDB seems to want from SSPL today.  By coincidence, those old licenses also work well for some newfangled components, like front-end JavaScript libraries and mobile app frameworks.  Companies routinely choose weak-copyleft licenses for those components to avoid simply handing their competitors the stick with which to beat them.  Some  start foundations, like Mozilla and Eclipse, that write their own terms instead.  Netscape had it in for Microsoft, and begat Mozilla, which wrote [MPL].  IBM had it in for Sun, and begat Eclipse, which wrote [EPL].  MongoDB has it in for AWS today, and wrote SSPL.

Failure to see past the superficial resemblance to Commons Clause, recognize that both MongoDB's and Common Clause users' business needs translated to weak copyleft, and guide them along that path turned a once-a-decade license-collaboration opportunity into a big, hot, angry ruckus.  SSPL's submission to the Open Source Initiative became a contest to see who could denounce MongoDB, alone or as symbol of venture capital finance generally, from the tallest bully pulpit.  Several folks interested in the nuts and bolts of the license fled to private correspondence, in dismay.

Instead of guiding and educating a public company evidently willing to bankroll much-needed open license maintenance that would have benefited many others, the self-styled brain trust of open source licensing, driven largely by non-lawyer activists, rejected MongoDB's stated motives out of hand.  The companies behind Commons Clause evidently couldn't afford or approve the project of modernizing weak copyleft for service components.  But their public-company forerunner, MongoDB, could, would, and did.

MongoDB got a chance to make its arguments, but those arguments never got a chance to be heard as presented and considered on their merits, at least through OSI.  If MongoDB had known [what kinds of preconceptions](http://lists.opensource.org/pipermail/license-discuss_lists.opensource.org/2019-February/020266.html) [awaited them there](https://anonymoushash.vmbrasseur.com/), they wouldn't have come calling to begin with.  The OSI mailing list couldn't separate the license proposed from prior conclusions about the party proposing it, and devolved into a largely unstructured, performative pillory.  Critics were often too invested in berating MongoDB for what it was---a newish company, rather than an [old corporate friend](http://redhat.com/) or [foundation](https://fsf.org)---or what they took it to represent---a sock-puppet for nefarious venture capitalists---to hear what it had to say, much less give benefit of the doubt or steel-man its license text.  Instead of scratching the surface, OSI's mailing devolved, yet again, into a [meta discussion about its own process](https://opensource.org/LicenseDiscuss022019).  There is still nothing close to consensus on whether who submitted a license should matter at all.

So MongoDB dug in on a license written almost entirely by its own hand, without significant outside contribution, that attends only to its own immediate needs.  They brought an olive branch, and got poked in the eye with it.  Understandably, they've had enough of that kind of feedback.

I had, too.  So I quit the OSI license-review process, and unsubscribed from its lists.

## Next

TODO
