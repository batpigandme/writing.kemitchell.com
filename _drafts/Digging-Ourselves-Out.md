---
title: Digging Contracts Out of the Hole
description:
layout: post
tags:
- Common Form
- Contracts
- Law
---

Fellow deals lawyer, how many different choice-of-law clauses did you send out last year?

I have no idea, myself, and for a professional wordsmith, I feel a bit a fraud.  Sure, choice-of-law is pretty humdrum.  But especially so, shouldn't I have _one_ choice-of-law clause, the best one I know of, for each state whose law I tend to choose?  Bolt-on nondisclosure sections.  Warranty disclaimers.  Indemnities.  Indemnity procedures.  So many bits and pieces, all suspiciously _diverse_.  When I'm sending out turn one, shouldn't my best work read more consistently, across deals and over time?

I don't know how many choice-of law clauses I sent out last year. But I will know this year. I've invested countless hours building tools.  Tools to make it more efficient to use my best than not to.  Tools for sharing and reusing work.  I want to put those tools in the hands of ever lawyer, right now, for free.

# Why?

As transactional lawyers, we understand the piece-part structure of contracts.  That understanding is universal in the practice, but not really shared, not effectively leveraged.  The most glaring manifestation is our failure to collaborate even with ourselves, on an individual basis, over time.  The costs of remembering what I've done before, and actually redeploying it, often outweigh the benefit I expect from replacing probably-good-enough with my current best.  Which is how so many of us end up hocking contracts made to order, but from wilted, rotten language, and feeling like circumstance robs us of the chance to feel personally expressed in our work every time. Even as our clients wince at the cost.

First-person failure sets us back a long way from effective collaboration.  Ideally, deals law would be a more social affair, with robust intercourse in ingredients, recipes, tools, and methods stoking competition at the cutting edge.  In other words, a bit more like other master-level pursuits, from cookery to carpentry, no less complex at their pinnacles, and often just as competitive.  Even when defined by competition, as in sport, other endeavors exact less collateral, personal damage, because camaraderie between bouts makes the practice itself rejuvenative.  Meanwhile, gaggles of lawyers flee their offices for bars also full of lawyers, where we drink and kvetch among the fellow afflicted to take out the sting of the day. Substance-abuse CLE and other symptomatic treatment won't dig law out of its lonely hole.

# Picks & Shovels

Maybe, long term, Ken Adams ends up writing all our indemnification provisions, and contract drafting looks more like building an outfit from clothes from a catalog than altering bits found secondhand.  That would certainly work out more efficiently.  But how will Ken's work make its way into our own?  When Ken's views evolve---along with his language---will we all have to copy and paste from a blog or a book into a million far-flung Word documents?  How will we disagree with him, if he's wrong?  How will the next Ken Adams start _their_ schism, and publish their own ready-made components?

Computers. The computers will do it. Not because "use the computer" is the answer to everything. But because they're ideally suited to the task. Not by intelligence. Computers are fundamentally dumb machines, and know nothing of contracts or their structure. But a few simple tools, understandable by people and applicable by machines, bridge the gap.

## Typing Convention

Microsoft Word is where content goes to die. The only universally practiced way of moving text in and out of Microsoft Word is copy-and-paste. Copy-and-paste is as rote as it gets. When we paste clauses into our contracts, we know we can never stop there. There's formatting to do. Definitions and references to check. Terms to replace. Blanks to fill. Alternatives to choose. Computers are capable of all of that mechanical work, if only they could recognize section structure, and which bits of text are definitions or other elements that need to be checked and conformed.

To enlist the computer's help, we need a way to tell it about structure, and not just about the text. In particular, we need a way to describe the boundaries of sections, articles, and other subdivisions, as well as where key structural elements, like defined-terms, definitions, references, blanks, and headings appear. We can do that with very simple typing conventions. For example, a definition from a data processing agreement under GDPR:

```text
""Restricted Transfer"" means a transfer of <Company Personal Data> from any <Company Group Member> to a <Contracted Processor>, or an onward transfer of <Company Personal Data> from a <Contracted Processor> to a <Contracted Processor>, or between two establishments of a <Contracted Processor>, in each case, where such transfer would be prohibited by <Data Protection Laws> (or by the terms of data transfer agreements put in place to address the data transfer restrictions of <Data Protection Laws>) in the absence of the <Standard Contractual Clauses> too be established under {Terms for Restricted Transfers} or {Restricted Transfers}.
```

Terms in double-double quotes, like `""Restricted Transfer""`, indicate definitions. "Restricted Transfer" is being defined there.

Terms in angle-brackets, like `<Company Personal Data>`, indicate uses of defined terms. "Company Personal Data" is defined elsewhere.

Terms in curly braces, like `{Terms for Restricted Transfers}`, indicate references to other parts of the document, by heading.

Some provisions, such as this clause from a stock purchase agreement, need fill-in-the-blanks:

```text
Subject to this agreement, on the date of this agreement or on another date agreed on by the parties (the ""Purchase Date""), the <Company> shall issue and sell to <You>, and <You> shall purchase from the <Company>, [Number of Shares] shares of the <Company>'s common stock (""Your Shares"").
```

Placeholders in square brackets, like `[Number of Shares]`, indicate fill-in-the-blanks.

These conventions enable computers to check that all the terms try to use are defined, that you define each term only once, and that every section you reference exists in your document. With  data showing the section-and-heading structure of your document, computers can number and format documents automatically. No more technical edits.

For an example, here is a commercial NDA with all its structural elements typed out:

<https://commonform.org/edit?from=ad495b6fc0492c7faa7d95d3e24df376972219fd4c436b51bc1d3dcc022e9237>

Here's the same form, formatted handsomely for the World Wide Web:

<https://commonform.org/rxnda/b-2w-b2b/1e1c>

And the same, automatically formatted for Word:

<https://commonform.org/rxnda/b-2w-b2b/1e1c?format=docx>

We can go further, and use the computer to perform routine checks on content. Here's an orthodox settlement agreement under California law, automatically annotated with feedback about archaic terms, wordy phrases, and guidance from _A Manual of Style for Contract Drafting_:

<https://commonform.org/forms/6e9a4a77f935b30123b86047fab3e56a5fa561a63c0e6a6789e527b473567ebb>

Those checks can be performed, by the computer in real time, as you draft.

That real-time experience will change the way you draft contracts. Forget about formatting. Forget about numbering. Forget about keeping lists of defined terms, or a table of contents. Computers are better at those things than you are, no matter who you are. You have better things to think about. And you'll find yourself making fewer and fewer mistakes, with real-time feedback.

All these tools are free to use, on [commonform .org](https://commonform.org). If you'd like an account for saving drafts to the site, [send me an e-mail](mailto:kyle@kemitchell.com).

## Components

Typing out contract language in a consistent, computer-understandable way makes it easier to share. 
But it doesn't necessarily make reusing language more efficient. You can paste language into a form on [commonform.org](https://commonform.org), and you'll get immediate feedback about structural problems it has, in context. But any kind of copy-and-paste remains a very manual process. It doesn't do enough to make sharing, reusing, and updating bits of language automatic and seamless.

Folks with accounts on [commonform.org](https://commonform.org) can save work to the site in two ways. One works a bit like private documents on a service like Google Docs: Save a form to the site, receive a link to the form that you can bookmark, and either keep private or share. But account holders can also publish forms under their own names, for everyone to find. Here's a list of forms that I've published under the account `kemitchell`:

<https://commonform.org/kemitchell>

I published each of those forms under my account name, as well as a project name. Some of those forms, like `safe-discount`, a startup investment instrument, and `slipstream`, an agreement for software-as-a-service and licensing, are complete documents. But other publications are mere components, meant to be reused in many forms. For example, here is copyright "work made for hire" clause, with an exception to avoid a bad result under California employment law:

<https://commonform.org/kemitchell/work-made-for-hire-unless-employment/1e1c>

I've used that component in the intellectual property section of one of my forms, `fairshake`, a plain-language independent contractor-consultant contract:

<https://commonform.org/kemitchell/fairshake/1e1u2d#heading:Intellectual%20Property>

The site displays not just the text of the component, but also sign that it _is_ a component, and who published it.

You may also notice that the terms of the component in my form aren't _exactly_ the same as the terms in the component. The component itself uses the terms "Work" and "Party Making Work". The form has replaced those terms with "New Intellectual Property" and "Contractor", the terms used throughout that form.

Thanks to the typing conventions, [commonform.org](https://commonform.org) knows which parts of the component are term uses. It also knows which terms have been defined elsewhere in the form. It knows that the form reuses the work-made-for-hire language as a component, inserts its text automatically, and handles replacement of terms and references to make it fit in. If the component contains _other_ components, it can handle insertion and replacement of those components, as well.

The system works a bit like incorporation by reference, but the computer automatically turns references into text. When you read a form that uses components on [commonform.org](https://commonform.org), you see both the text of each component, and also a note that it comes from a component. When you download a Word copy, the notes disappear, and all you see is one, whole, internally consistent document.

## Updates

Typing conventions and components make everyone with a [commonform.org](https://commonform.org) a legal publisher, as well as a power-shopper of legal language. If I publish my preferred limitation of liability, anyone can seamlessly incorporate it into their own work as a component.

What happens when I find a way to improve my standard limitation of liability, and publish a new edition of my terms?

[commonform.org](https://commonform.org) uses a system called [Reviewers Editions](http://reviewersedition.org/) to number updates. There are four kinds of numbers: editions, updates, corrections, and drafts. The Reviewers Edition `1e` means "first edition". `1e2u` means "second update to the first edition". `3e2d` means "second draft of the third edition".

As publishers update their language, they increase a Reviewers Edition number for each new update. Which number they increase sends a message about the kind of changes they've made. When a publisher increases the edition number, say from `2e` to `3e`, they tell others using that language should review the whole new third edition, to make sure it still meets their needs. When a publisher increases an update number, say from `5e1u` to `5e2u`, they tell users of `5e1u` to compare to the new update, and review the parts that changed. Increasing a correction number, say from `4e2u` to `4e2u1c`, lets users know that _everyone_ using `4e2u` should use `4e2u1c` instead, often because it fixes a spelling or structural error. Drafts allow publishers to float new changes for discussion, without telling anyone to use the new language yet.

Reviewers Editions primarily help drafters communicate change to other drafters. But computers can understand the basics of their meaning, too.

For example, forms on [commonform.org](https://commonform.org) that use components can choose to use either specific versions of those components, or to automatically update to utilize any corrections. The `fairshake` consulting form I mentioned above uses `kemitchell/work-made-for-hire-unless-employment/1e1c` with automatic updates. If I find a typo in `1e1c` tomorrow, and publish a new `1e2c`, `fairshake` will incorporate that fix automatically. So will any other form on [commonform.org](https://commonform.org).

Anyone with a [commonform.org](https://commonform.org) account can subscribe to notifications about the forms they publish. The website notifies them whenever the publisher of a component in those forms publishes a new update. They can [compare new language to old](https://commonform.org/compare/5fd90cf89aa4ee976583c0183dd6660a72bf22e86a3be0e8913f6622328fe24a/1b048f6c4cf0df69e364dd8bcc93a792b644aef243398d463a6202d1a0dbd43c), make a decision, and update their forms accordingly\