---
title: Reading the Open Source Definition as Copyleft Regulation
description: an in-depth review of minor limits and recurring errors
layout: post
tags:
- SSPL
- Open Source
- Licensing
- Copyleft
---

This is the second in [a series inspired by MongoDB's Server Side Public License](/series/SSPL.html) and ensuing debate.  It builds on [the first](https://writing.kemitchell.com/2018/10/24/How-to-Speak-Copyleft.html), which sets out the vocabulary of copyleft design and regulation used here.

------

How does the Open Source Definition regulate maintenance of strong copyleft terms in open source licenses?  Sporadically, incompletely, and unhelpfully for current controversies.  A few Definition criteria set specific limits, but most don't say anything about copyleft at all.  A few, read out of context, beg readings that prohibit all copyleft licenses generally, clogging up debate.

In reading the Definition as a copyleft regulation, we can ask three specific questions:

1. Does the Definition prohibit specific language in open source copyleft licenses?

   For example:  Does the Definition prohibit use of the term "restriction"?

2. Does the Definition prohibit specific copyleft design choices for trigger, reach, licensing, or distribution?

   For example:  Does the Definition prohibit triggering on running software without changes to provide network services?

3. Does the Definition prohibit copyleft design approaches more generally?

   For example:  Does the Definition prohibit designs that trigger on network use and reach beyond derivative works of the licensed software?  Designs that seem too strong, in some other way?

In the end, the Open Source Definition provides neither holistic design-approach regulation, nor regulation for each copyleft design choice.  That makes the Definition an incomplete copyleft regulation, at best.

That is altogether understandable, considering the way it was written, and why.  The Definition wasn't meant to answer current questions about the limits of copyleft design.  They hadn't even been practically posed yet.  But we're asking them  now.  In order to establish meaningful regulation for open source copyleft, we'll have to look past the Definition.

In another post in this series, I'll do just that, to offer a usable framework.  This post, however, will cover only what we can glean from the text of the Open Source Definition, its history, and the licenses the Open Source Initiative has approved as conforming.

Here's the plan:

1. [Review the criteria that clearly regulate copyleft.](#clear-copyleft-regulations)
2. [Review a few common interpretive traps.](#interpretive-traps)
3. [Consider the redistribution criterion, as a warm-up.](#redistribution)
4. [Dive into the discrimination criteria, first field-of-endeavor, then person-or-group.](#discrimination)
5. [Round out with the contamination criterion.](#contamination)

## Clear Copyleft Regulations

Three Open Source Definition criteria---3, 8, and 10---clearly regulate copyleft design choices.  Starting with those will give us a sense of the kind of clarity we won't find in other criteria.

### Allow the Same Terms for Derived Works

Criterion 3 of the Definition was brought over from the Debian Free Software Guidelines without change:

> **3. Derived Works**
>
> The license must allow modifications and derived works, and must allow them to be distributed under the same terms as the license of the original software.

Criterion 3 is a clear regulation of licensing design choice.  To be open source, a copyleft rule must at least allow the same license terms for work within its reach.  It can't require different terms, such as permissive terms or terms that aren't open source.

It's not clear from the text of the Definition whether the same terms must be the _only_ terms on which "derived works" can be licensed.  That was true of GPLv2, which the Definition, like the Debian Free Software guidelines from which it derived, were meant to describe.  However, there are three are three pieces of compelling evidence against requiring the same terms, rather than merely allowing them among other choices.

First, criterion 3 says that the license must "allow" the same terms, not that the license must "require" them.

Second, permissive licenses like BSD, another license listed in the "Example Licenses" section of the Debian Free Software Guidelines, permit distributing "derived works" under any terms.  There's no reason evident from the text of the Definition why permissive licenses should be able to allow permissive "derived works", but copyleft licenses should not.

Third, the Open Source Initiative has approved licenses that permit different terms for at least parts of "derived works".  For example, section 13 of GPLv3 and section 13 AGPLv3 create a compatibility bridge between those licenses, by making exceptions to their licensing rules for keeping GPLv3 and AGPLv3 contributions under their respective terms.

### No Product-Specific Licensing

Criterion 8 of the Debian Free Software Guidelines had to be generalized for the Open Source Definition:

<blockquote><p><strong>8. License Must Not Be Specific to <del>Debian</del><ins>a Product</ins>.</strong></p><p>The rights attached to the program must not depend on the program’s being part of a <del>Debian system.</del> <ins>particular software distribution.</ins> If the program is extracted from <del>Debian</del> <ins>that distribution</ins> and used or distributed <del>without Debian but otherwise</del> within the terms of the program’s license, all parties to whom the program is redistributed should have the same rights as those that are granted in conjunction with the <del>Debian system.</del> <ins>original software distribution.</ins></p></blockquote>

If we read "software distribution" and "product" to cover not just distributions of multiple programs, like Linux distributions, but also particular distributions of the licensed program itself, like Firefox and Iceweasel, criterion 8 becomes a clear regulation of licensing copyleft design choices.  An open source copyleft rule cannot vary the terms required for parts taken out of the program and parts left with or as a part of it.

### Technology Neutrality

Open Source Definition criterion 10 was not part of the Debian Free Software Guidelines, which included an "Example Licenses" section as number 10, instead.  Here is the new text, peculiar to the Open Source Definition:

> **10. License Must Be Technology-Neutral**
>
> No provision of the license may be predicated on any individual technology or style of interface.

Criterion 8 is a clear regulation of distribution and licensing design choices.  An open source copyleft license cannot require licensees to use a specific technology for licensing or distributing code within its reach.  For example, an open source copyleft license cannot require licensees to distribute work within its reach via FTP, or to require that licensees for derived works accept terms for that work by electronic signature.

<!-- TODO: Notes on categories of methods -->

## Interpretive Traps

The text of Open Source Definition is admirably terse and perhaps inevitably ambiguous, affording several plausible readings of each criterion.  There is not enough in the Definition itself to narrow down to just one evidently correct meaning per requirement.  To select from among plausible meanings, we have to look past the page.

Some readers forget to look _outside_ the text, and fixate on readings that don't make sense in the context of the Definition's history.  Others read between the lines, arriving at conclusions that very general language nonetheless has one very specific meaning.

Before diving into the other Definition criteria that typically crop up in strong-copyleft discussions, it's worth reviewing those interpretive traps, as we'll find them in a more than one criterion, later on.

### Excluding Copyleft Generally

Ignoring history, it's possible to read several criteria of the Open Source Definition, straight off the page, to prohibit copyleft altogether.  These readings crop up each time a new, stronger copyleft license appears, forcing large parts of the conversation to start from before square one, rather than from where the debate left off the last time.  The generality of the Definition invites these readings.

Generality was intentional.  In fact, generalization was the point.  The Open Source Definition was adapted from the [Debian Free Software Guidelines](https://www.debian.org/social_contract#guidelines), which were made part of the [Debian Social Contract](https://www.debian.org/social_contract) in 1997.  The Debian Project drafted and adopted the Guidelines to describe the kinds of licenses project participants recognized and accepted at that time, as a category of license terms.

That category included [GPLv2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html), then considered a very strong activist copyleft license, and a very popular choice.  A section of the Guidelines entitled "Example Licenses", removed in the Definition but still a part of Guidelines, lists "GPL" first.  The Open Source Initiative approved GPLv2 under its adaptation of the Guidelines.  Thus, as a threshold matter, any reading of any criterion of the Open Source Definition that excludes GPLv2 can't reflect the meaning of the Definition.

The Open Source Initiative has since approved other, stronger copyleft licenses.  Readings of the Definition criteria that exclude those licenses can't reflect how the Definition has been understood since.

### Oddly Specific Readings of Very General Language

Starting from a reading of some Definition criterion that limits copyleft and paring back to avoid GPLv2 or subsequently approved licenses, it's possible to end up with a very specific reading that limits open source copyleft in a very specific way.  But it is only the history that leads to that specificity.  The text of the Definition remains as general as it was the day it was published.  The path from general text to highly specific meaning is not apparent or inevitable.

This error often manifests as the position that the outer limit of open source copyleft is whatever the last approved stronger-copyleft license happened to be, damning every new, yet stronger copyleft proposal, in succession.  Starting from what's new is better than starting from whether copyleft can ever conform to the Definition.  But looking back at a general Definition, plus a history of progressively stronger approved copyleft licenses, it never follows that the last approved stronger-copyleft license has to be the last ever.  That debate has to reach beyond the Definition and even Open Source Initiative history, to the industry, community, and history of the movement.  It has to take into account that the Open Source Initiative only definitively accepts licenses, declines to approve many licenses that conform to the Definition, and never affirmatively and finally rejects any terms.

The concept of precedent proper remains highly controversial among license-review participants.  On the other hand, there doesn't seem to be any will to remove or deprecate licenses approved in the past.  It's clear that past decisions, and especially use of approved licenses in apparent reliance on Open Source Initiative approval, always seems to matter for new submissions.  It's just not clear how.

The error made with highly specific readings of admittedly general Definition text that rely on past decisions and history isn't that they're necessarily wrong.  The error is in claiming that the wording of the Definition compels them.  There may be very good reasons for such specific rules, but they aren't in the Definition.

### Restriction versus Condition

Some open source license specialists distinguish "restrictions", which hold back permission to take actions governed by licenses, from "conditions", which add requirements to meet after doing what's permitted.  The word "restrict" appears six times in the Definition, but it doesn't mean "not a condition".

Specialists speak of prohibitions on copying, distributing, or using software for commercial purposes as "restrictions".  A noncommercial license has a commercial use restriction.  Conversely, they speak of notice-retention rules, which require keeping copies of copyright notices and license terms with copies of software, as "conditions".  Copyleft rules, which require sharing source and giving a license, are almost always classed conditions, too.

The terms "restriction" and "condition" thus serve a helpful shorthand function in open source licensing jargon.  Unfortunately, that function leads us right into a circular argument.  Restrictions are always bad, and suggest that a license isn't open source.  Conditions do not.

It’s not at all clear that the Definition means “restrict” in that oddly particular way.  The word "condition" never appears in the Definition.  Both the Debian Free Software Guidelines and the Open Source Definition predate today's larger community of open source licensing specialists, and may predate this jargon usage, too.  The restriction-bad, condition-good association may in fact stem from the Definition, at least partially, explaining its apparent circularity.

But perhaps the distinction in jargon reflects a distinction in the law that affects software licenses?  After all, many of the licensing specialists who use the distinction come from the legal camp.

To enforce a copyright license for software, copyright holders bring lawsuits for, among other things, copyright infringement: claims that others took action controlled by copyright without a license from the copyright holder.  For an infringement lawsuit based on copyleft, the claim is that the licensee went beyond the permission they received under the public license by failing to distribute source code reached by the license, and licensing it as specified, after triggering the requirement to do so.  Whether a defendant lacked permission because the license restricted distribution of closed source---sounds like a "restriction"---or because they had permission to distribute source broadly, but failed to meet an additional requirement of making it open source---sounds like a "condition"---the legal claim is copyright infringement.

In the end, a copyright license creates a list of things that a licensee can do with a work of copyrighted software.  Every action covered by copyright but not permitted by the license or a legal exception, like fair use, remains infringement.  Either the license gave permission to do what the defendant did, or the defendant committed infringement.  Whether we call a license rule a restriction or a condition, it reduces the amount of permission granted by a license.

If the difference between "restriction" and "condition" isn't in what counts as infringement, perhaps it's in the consequences.  I've heard some lawyers explain it in terms of legal "remedies": what you can get from a court when you win a lawsuit.

Successful copyright infringement lawsuits lead to court orders for defendants to stop taking action with the software.  Courts issue orders to stop making and distributing proprietary software in a way that breaks a copyleft rule.   However, at least under US law, it's not at all clear that courts will order defendants to fulfill conditions, say by forcing defendants to distribute their source code and license it as required to satisfy a copyleft rule they broke.  Likewise if terms get enforced as a contract, instead of or in addition to being enforced as a copyright license.  It's far more likely that courts will order defendants to stop working with the copyrighted software and award money damages as compensation for the infringement.

In other words, under US law, we expect courts to award money, not code.  Legal confusion on this point contributed to the fear, uncertainty, and doubt about copyleft licenses as "viral" licenses that could force large companies to share their closed software.

At this point, we are deep in the law.  All of this speaks from legal background that neither the Definition's author nor its audience had at the time.  Even if there were a clear legal distinction between restrictions and conditions, based on legal remedies or otherwise, it’s not at all clear that the Definition means “restrict” in that oddly particular way.  The Definition describes licenses, which are legal tools.  But the Definition doesn't speak in the terms that US lawyers would choose.

## Redistribution

Having covered some common interpretive traps, let's have a look at the first Open Source Definition criterion that repeatedly snares readers.

Open Source Definition criterion 1 reads more or less as criterion 1 of the Debian Free Software Guidelines did:

<blockquote><p><strong>1. Free Redistribution</strong></p><p>The license <del>of a Debian component</del> <del>may</del> <ins>shall</ins> not restrict any party from selling or giving away the software as a component of an aggregate software distribution containing programs from several different sources. The license <del>may</del> <ins>shall</ins> not require a royalty or other fee for such sale.</p></blockquote>

We could strain to read criterion 1 as a rule against licenses whose reach and licensing terms create license compatibility issues.  In other words, copyleft rules that create conflicts with other copyleft rules, preventing developers who combine work under both licenses from sharing the combination together.

We'd have to read "component" and "aggregate software distribution" to cover changed versions and programs based on the licensed work.  Considering that "derived works" gets used for this meaning in another, dedicated criterion, that seems a stretch.  And I don't think developers in practice would go out of their way to say "component of an aggregate software distribution" when they meant "part of a new program" or "basis of a new version".

But even if we accepted that interpretation, we'd end up with an [oddly specific reading](#oddly-specific-readings-of-very-general-language) that we'd have to pare back to save GPLv2.  GPLv2 has created plenty of compatibility problems.  Arguably, it invented modern license incompatibility.  But there's no basis in the text for paring the broad reading back to save it.  Criterion 1 says "restrict", and GPLv2 is full of "conditions".  But as [described above](#restriction-versus-condition), there's no good reason to read the specialist distinction between "restrictions" and "conditions" into the Definition generally, or condition 1 specifically.

Overall, "redistribution" here seems to mean something far more like sharing collections of software than changing or building it.  We'll see that again in the [contamination](#contamination) criterion, later on.

## Discrimination

Two Open Source Definition criteria, 5 and 6, prohibit discrimination, the first against "any person or group of persons", the second against "specific fields of endeavor".  Yet those criteria don't prohibit copyleft, even though copyleft always discriminates, by design.

Quoting Richard Stallman, from _Copyleft: pragmatic idealism_:

> I make my code available for use in free software, and not for use in proprietary software, in order to encourage other people who write software to make it free as well.  I figure that since proprietary software developers use copyright to stop us from sharing, we cooperators can use copyright to give other cooperators an advantage of their own: they can use our code.

That is discrimination.  We might also call it reciprocity, fair play, or the golden rule in action.  But it is discrimination.

Evidently not the _kind_ of discrimination the Definition prohibits.  The Open Source Initiative has approved all of the major licenses drafted by the Free Software Foundation, which Stallman founded.

### Field of Endeavor Discrimination

Criterion 6 of the Open Source Definition reads:

> **6. No Discrimination Against Fields of Endeavor**
>
> The license must not restrict anyone from making use of the program in a specific field of endeavor.  For example, it may not restrict the program from being used in a business, or from being used for genetic research.

This language was copied from the Debian Free Software Guidelines verbatim.

Ignoring open source licensing history, it's possible to read criterion 6 to prohibit all copyleft licenses whatsoever.  After all, as a practical matter, copyleft terms prevent use of copyleft software in the creation of closed software.  That tracks the general meaning of "discriminate".  Per the Oxford English Dictionary:

>  _intransitive_. _Economics_ (orig. _U.S._). To treat goods, trading partners, etc., more or less favourably according to circumstances.  Frequently with _against_ (also _in favour of_). Also in prepositional passive with _against_.

How can we square that reading with a long list of approved copyleft licenses? Different readers answer that question differently.  Some focus on "restriction".  Some focus on "making use".  Some focus on "specific field of endeavor".

Overall, natural readings of "restrict" and "making use" are very broad.  So broad, in fact, that they describe GPLv2.  But "specific field of endeavor" doesn't have any everyday meaning.  If we read it broadly, it works with the other key terms to exclude GPLv2, which can't be right.  But if we track the examples, focusing on endeavors where open or closed is a choice, we end up with a reading that works.

#### Restrict

> The license must not **restrict** anyone from making use of the program in a specific field of endeavor.

In ordinary English, the meaning of "restrict" is very broad.  Per the Oxford English Dictionary:

> To limit (a person or thing); to confine _to_ or _within_ certain limits.
>
> To prohibit or prevent _from_.

Applying this ordinary meaning, “restrict anyone from making use of the program in a specific field of endeavor” would cover rules that turn “making use” in a “specific field of endeavor” into infringement, however that’s accomplished.  Considering GPLv2, the question would then become how we read “making use” and “specific field of endeavor”.

As [described earlier](#restriction-versus-condition), it's hard to argue that the general distinction between "restrictions" and "conditions" among licensing specialists applies in criterion 6, instead of the ordinary meaning.

#### Making Use

> The license must not restrict anyone from **making use** of the program in a specific field of endeavor.

##### Ordinary Meaning of Making Use

The everyday meaning of “use” is extremely broad, covering anything licensees might do with software.  Following that meaning, “restrict anyone from making use of the program” would describe copyleft conditions that prevent licensees from distributing copyleft software with closed changes, as part of closed programs, or simply under different, closed terms.  The question becomes whether distributing closed software is a “specific field of endeavor”.

##### Actions Governed by the License

Some read “making use” in criterion 6 to mean specifically taking any action controlled by the license, under intellectual property law.  Under copyright law, that means, broadly speaking, making copies, publicly distributing copies, and making changes or new work based on the old.

Trigger language for all kinds of conditions in old open source licenses usually speaks in terms of publicly distributing copies, making changes or new software based on the licensed software, or both.  Both of these actions are controlled by copyright, and governed by copyright licenses for software.  Triggers in the earliest copyleft conditions, like GPLv2's, also speak in terms of these actions.  This reading of "making use" would therefore catch GPL.

##### Running the Software

Some read "use" even more specifically, to mean one specific kind of use: "running" or "executing" software.  This reading misses early, GPLv2-style copyleft licenses, because those licenses triggered copyleft only on distribution or making changes or new software based on the licensed software, not running the licensed software.  But it would catch stronger, network copyleft licenses that OSI has already approved.

Under copyright law, owners of copyright do _not_ have an explicit right to control and license running of their software.  However, copying software is an unavoidable step in running it, for installation, loading into RAM for execution, and so on.  Since copyright holders _can_ control copying of their software, they have indirect power to control running of their software.  A [specific section of US copyright law](https://www.gpo.gov/fdsys/search/pagedetails.action?granuleId=USCODE-2017-title17-chap1-sec117&packageId=USCODE-2017-title17&fromState=) makes an exception to this rule, for copies of software that users own, especially when purchased as a part of a package, with a computing device, to keep it running as delivered.  But [well known federal case law](https://en.wikipedia.org/wiki/Vernor_v._Autodesk,_Inc.) indicates that having a license, especially one imposing notable use restrictions, is not the same as owning a copy.

Copyleft licenses approved after GPLv2, in particular “network copyleft” licenses that trigger on provision of the software as a service to others over a network, go beyond distributing, making changes, and building new software, explicitly or implicitly.  They cover running it.  Some, like [OSL](https://opensource.org/licenses/OSL-3.0), actually say "use" in their trigger language.  Others, like [AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html), seem to take great pains to avoid saying "use", "run", or "execute" in their triggers.

Regardless of wording, a copyright license can only control the actions covered by copyright.  Providing services to others over a network is not distributing copies publicly or making changes or new work based on the software.  In fact, copyleft rules based on providing network services _ensure_ that licensees distribute, when they otherwise haven't.  The only action governed by copyright that remains as a possible basis for those rules, then, is copying.  When a copyright license makes rules about running a program, it makes rules about making copies, as one must to run the program.

I've heard from a few commentators that the language of AGPL, an early network copyleft license, was meant to create a kind of "public performance" right for software.  Public performance is another action controlled by copyright.  Licenses for other kinds of copyrighted work, like film, theatrical, and musical works, control public performance of those works.  Technically, software licenses also control public performance of software, but what public performance means for software remains unclear.  The authors of AGPL would have liked public performance to clearly cover running software for others to interact with over a network, but it did not, and it still doesn't.  So they wrote a license condition that provided similar effect.

Copyright licenses conditions attempting to control rights other than those controlled by copyright law have to fall back on control of the actions copyright law does control.  In the case of "synthetic" public performance rights---what lawyers would call "constructive" public performance rights---that means falling back on control of running the software, via control of copying the software.

Either way, a reading this specific strays a long way from the general text of the Definition.  Criterion 6 says "making use", which is not a legal term.  For more specificity, it could have easily said "running" or "executing", and all involved would have known what was meant.

Taking "making use" to mean specifically running the program, but not publicly performing the software, or not providing the software to others over a network, is even more specific, and also anachronistic.  Neither the need for such a fine-grained distinction, nor any particular implementation of it, were pressing issues at the relevant times for the Guidelines or the Definition.

#### Specific Field of Endeavor

> The license must not restrict anyone from making use of the program in a **specific field of endeavor**.

If we count copyleft rules as “restrictions”, and accept that open source copyleft licenses trigger on “use”, we could still decide that proprietary software development doesn’t count as a “specific field of endeavor”.  That would explain how approved copyleft licenses from GPLv2 on conform to criterion 6.

##### Any Activity at All

If we read "specific field of endeavor" to mean any specified activity at all, at any level of generality, it comes to include development and distribution of closed software.  Unless we adopt one of the improbable meanings of "restrict" or "making use", such a broad meaning of "specific field of endeavor" would exclude GPLv2, the license that both the Guidelines and the Definition clearly meant to include.

##### Legal Meaning

The term “field of endeavor” has no specific meaning in intellectual property law.  The term does appear in US immigration law, but again, there’s no reason to believe the Definition means to invoke that usage specifically, or any legal meaning, to begin with.

##### Fields with Choice of Open or Closed

If we read "restrict" and "make use" in the ordinary, natural ways, "specific field of endeavor" can't mean closed development.  At a minimum, GPLv2 restricts companies from using GPLv2 code in closed sourced that they distribute to others.  Later, stronger copyleft licenses restrict companies from using copyleft code in closed source in other ways, like providing network services.

The Open Source Definition and software licensing history provide a number of examples of specific fields of endeavor that fit the history of copyleft approvals.  Criterion 6 mentions business and genetic research.  Software licenses prohibiting military use have been widely considered non-conforming, as have licenses prohibiting use in violation of human rights.

OSI's annotated Definition reemphasizes commercial use.  As all major open advocacy groups, including OSI and FSF, have enthusiastically urged, "commercial" and "closed" are not synonymous, any more than "noncommercial" and "open".  Many people and firms, in many industries, produce, distribute, and develop open source software for pay or other commercial advantage.  Business firms, genetic researchers, and military personnel can employ and make open as well as closed software.  Software is but a means to those endeavors.  The choice of open or closed, as user or developer, stands independent of the choice to endeavor in those specific fields.

Some firms do business in software development primarily.  Many of those develop or consume closed software exclusively, for a variety of industries or other use cases.  But all firms face a choice of whether to take or make work on open or closed terms.  Activist copyleft was designed to create incentives to choose open, by excluding firms that choose closed.  The Definition was written in large part to describe one of those licenses, GPLv2.

Excluding closed software development doesn't mean locking "specific field of endeavor" down to just business or genetic research.  We could extrapolate to other fields that offer a choice of open or closed, such as hyrdraulic fracturing, alcoholic beverages, private prisons, the practice of law, and so on.

### Person and Group Discrimination

Open Source Definition criterion 5 reads:

> **5. No Discrimination Against Persons or Groups**
>
> The license must not discriminate against any person or group of persons.

This language was brought over from the Debian Free Software Guidelines without any changes.

Criterion 5 has typically been used to exclude licenses that blacklist particular people or firms by name, such as lists of firms or particular national governments.  Sometimes developers provided reasons for these lists, and sometimes  they turned the reasons into categories, excluding by description.

For any activity, we could define a group: the group of people performing that activity.  For example, the group of people developing closed software.  Discriminating against those people in those groups, by requiring them to develop software when they'd choose not to, or cannot, would disqualify approved copyleft licenses, including GPLv2.  That can't be right.

Approved licenses of all kinds---permissive and copyleft---discriminate against other people and groups on the basis of their choices.  Perhaps most notably, the defensive termination provisions of many licenses take back permissions granted by licenses to those who sue developers or users under patents.  Those rules are highly discriminatory against firms that actively enforce their patents.  They're especially discriminatory against firms that primarily acquire and sue on patents.  Those are evidently not the kinds of people or groups of people criterion 5 is meant to protect.

## Contamination

Open Source Definition criterion 9 involved a slight heading change:

<blockquote><p><strong>License Must Not <del>Contaminate</del><ins>Restrict</ins> Other Software</strong></p><p>The license must not place restrictions on other software that is distributed along with the licensed software. For example, the license must not insist that all other programs distributed on the same medium must be <del>free</del><ins>open-source</ins> software.</p></blockquote>

I've seen criterion 9 read to regulate copyleft reach and licensing.  But for the reasons that follow, I don't see those readings in the text and its history.

When discussing criterion 9, I find it's useful to bring all the interpretive boundaries up front:

1. However we read the first sentence of criterion 9, it needs to accord with the same-media example in its second sentence.

2. We can't read criterion 9 to exclude GPLv2, since the Definition was written to describe, not exclude, that copyleft license.  The last paragraph of GPLv2 section 2 mirrors the example in criterion 9:

   > In addition, mere aggregation of another work not based on the Program with the Program (or with a work based on the Program) on a volume of a storage or distribution medium does not bring the other work under the scope of this License.

3. Reaching now into history, criterion 9 can't exclude network-copyleft licenses like AGPL and OSL.

4. More controversially, criterion 9 evidently didn't exclude stronger-trigger copyleft or "reciprocal" licenses such as Plan 9, Open Watcom, and RPL, which were approved by the Open Source Initiative but rejected by the Free Software Foundation.

### Restrictions

As [noted earlier on](#restriction-versus-condition), it's tempting to fall back on an informal or potential legal distinction between "restriction" and "condition", but there's no cause to read Open Source Definition language in either of those specific ways.  The natural reading of "restrictions" is broad.

### Distributed

With "distributed", we have much the same interpretive problem as "use" in condition 6.  We could read it informally, to mean sharing software, or as a legal allusion to distribution to the public under copyright law, or as something in between.

But "distributed" in criterion 9 is more troublesome that "use" in condition 6, considering GPLv2.  Reading "use" to mean running software pointed to an action with software that GPLv2 did _not_ use in its copyleft trigger.  Even if we read "distributed" in criterion 9 in an oddly specific, legal way, that kind of distribution is the crux of GPLv2's trigger.  In other words, reading "use" specifically takes GPLv2 out of criterion 6, but reading "distribute" specifically leads to a meaning that would still exclude GPLv2.

### Other Software

Straining to make a copyleft regulation out of criterion 9 is a lot of work for little reward: "other software" would become the limit of copyleft reach.  That's not much to go on, and would also run immediately into problems with approved-license history.

GPLv3 reaches beyond the software itself:

> The “Corresponding Source” for a work in object code form means all the source code needed to generate, install, and (for an executable work) run the object code and to modify the work, including scripts to control those activities. However, it does not include the work's System Libraries, or general-purpose tools or generally available free programs which are used unmodified in performing those activities but which are not part of the work. For example, Corresponding Source includes interface definition files associated with source files for the work, and the source code for shared libraries and dynamically linked subprograms that the work is specifically designed to require, such as by intimate data communication or control flow between those subprograms and other parts of the work.
>

So does RPL 1.5:

> 1.12 "Required Components" means any text, programs, scripts, schema, interface definitions, control files, or other works created by You which are required by a third party of average skill to successfully install and run Licensed Software containing Your Modifications, or to install and run Your Derivative Works.

### Derived Work

License terms can break those rules.  They can grant permission only to distribute along with other open software, not proprietary.  They can require prominent billing on lists of contents of particular media on which they're reproduced.  Debian's infrastructure and software can't implement every rule-breaking license's terms in software, and ensure they're followed.  To prevent that explosion of complexity, which might make package distribution totally unworkable, Debian excluded software that creates those problems.

## Takeaways

We're asking the Open Source Definition to do more and different work than it was written to do.  Sitting nominally at the center of the Open Source Initiative process, reviewers look to it as the total framework for license analysis, describing and debating in its terms.  But when those debates reach copyleft design choices that the Open Source Definition simply does not address, its structure boxes discussion in, rather than structuring or supporting it.  We begin to force-fit our own broader thoughts and instincts about copyleft regulation---as I've been tempted to do throughout this post---into odd nooks and crannies, because they have to go somewhere.  All of this makes writing about copyleft regulation, and reading what others have to say, even harder.

We should accept that the Open Source Definition was written to generalize a broad category of licenses with very few strong copyleft examples, and strong cohesion around GPLv2.  We should accept that in its time, for its purpose, anticipating and resolving as yet theoretical problems in copyleft design would have been wasteful, foolish, and potentially dangerous to the movement then coalescing.  We should accept that the Open Source Definition offers at best an incomplete approach to regulating copyleft, and no particularly good vocabulary for expressing a complete one.

I agree with colleagues, some of whom reject strong-copyleft licenses I've drafted, that the Open Source Definition alone can't suffice as the whole basis for assessing new strong-copyleft licenses.  But I disagree strongly with the idea that an unwritten consensus on the limits of copyleft is latent in the Definition, for an elect who can see it, or that the Open Source Initiative or any other group should graft one onto the Definition, exclude those who disagree, and call the remainder consensus.  The way forward is acknowledging that licenses written to the Definition---in 2002 or 2017---conform to the Definition.  That doesn't mean the job of assessing the advisability of a license is done.  It means it's time to put down the Open Source Definition, as a tool, and either pick up or fashion a more specialized one, for the more specialized job of assessing new copyleft designs.

In posts to come, I'll set out guideposts for comprehensive regulation of copyleft in open source licenses.  I don't anticipate immediate, unanimous acclaim for every point in those posts.  But I hope even those who disagree will come to appreciate how freedom from the task of torturing copyleft rules into Open Source Definition, by exegesis fair or foul, makes the task writable.
