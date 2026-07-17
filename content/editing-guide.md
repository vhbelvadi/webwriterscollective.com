---
title: "Editing guide"
date: 2026-07-17T20:33:07+01:00
type: page
draft: false
---

This guide is intended for existing members of WWC who may wish to edit this website for the following reasons:
1. to post a notice to the noticeboard
2. to submit their contribution to *Anthologies*
3. to update their author bio and website
4. to help fix typos or make minor improvements across this website

# Prerequisites

A basic knowledge of git, or at least navigating around Github, is expected. If you do not believe you can continue with this, please feel free to send your contributions, or editing requests [via email](mailto:hello@vhbelvadi.com). While we cannot promise to update the website right away, we will try our best to do so as quickly as possible. However, please continue to read this guide as it will tell you what sort of document you need to send our way.

We use Hugo to run this website and therefore all contributions should be in markdown with `yaml` frontmatter. While some knowledge of Hugo can help if you run into trouble, you do *not* need to know Hugo to make contributions. You do, however, need to know Hugo (and Tailwind) to propose structural or functional updates to this website.

***

# 1. Posting a notice

Posting a notice is a three-step process: create the notice, type up the front matter (and contents) and finally push or submit the notice.

## 1a. Creating a notice

**If you are familiar with Hugo** clone [this website’s repo](git@github.com:vhbelvadi/webwriterscollective.com.git), install Hugo and any dependencies if you have not done so already, and create a new note by running the following command from the terminal:

```
hugo new noticeboard/your-notice-here --kind notice
```

This should give you file inside `content/noticeboard/your-notice-here` with the approproate front matter.

**If you are unfamiliar with Hugo** simply [download this file](/md-templates/notice/index.md) (or copy the contents displayed, depending on your browser) and work on it using your favourite text editor.

## 1b. Front matter

In the front matter for a notice, the following fields are compulsory:

- `title`
- `summary`
- `authors` is an array that should look like `["Jane Doe","Betelguese","John Smith"]` (see the *Updating your author page* below for more)
- `date` should take the format `yyyy-mm-ddThh:mm:ss±hh:mm` (the last `±hh:mm` is your timezone but leave it as `+00:00` if in doubt)
- `type` should be `notice`
- `draft` should be set to `false` (when you are ready to publish)

The file you created using Hugo, or downloaded above if you went that route, will have other front matter fields like `cover` and `subtitle` which are self-explanatory (or see FAQs below for more). An especially important, but optional, field is `external_link` which is useful if you wish to send people to your or another relevant website as part of your notice, e.g. for a subscription form or for examples of an ongoing project.

Type the main content of your notice after the `---` at the end of the front matter. There is no word limit.

## 1c. Publishing your notice

If you used Git and Hugo, simply submit a pull request to publish your notice. Frequent contributors may request to be added to the repo to bypass this step (we are a community after all).

If you downloaded the file above, simply e-mail the file to [James G](mailto:readers@jamesg.blog) or [V.H. Belvadi](mailto:hello@vhbelvadi.com) and we will publish it for you. However, we cannot promise to publish it within tight deadlines.

***

# 2. Contributing to *Anthologies*

The general steps for contributing to *Anthologies* is identical to posting a notice, but with a few important variations. While the steps are all detailed below, feel free to also consult the *Posting a notice* section above for additional guidance. Submitting an article is a three-step process: create the article, type up the front matter (and contents) and finally push or submit the article.

Articles will be published once an entire issue of *Anthologies* is ready. This is why we will be using the word ‘submit’ rather than ‘publish’ for articles going foward.

## 2a. Creating an article

**If you are familiar with Hugo** clone [this website’s repo](git@github.com:vhbelvadi/webwriterscollective.com.git), install Hugo and any dependencies if you have not done so already, and create a new article template by running the following command from the terminal:

```
hugo new anthologies/1/my-new-article --kind article
```

Make sure you change not only the article slug `my-new-article` but also the issue number `/1/` to correspond to the next issue (to which you are submitting). Check the [*Anthologies* page](/anthologies) to figure out what the upcoming issue number will be.

This command should give you file inside `content/anthologies/1/your-notice-here` (or whatever issue number you picked) with the approproate front matter.

**If you are unfamiliar with Hugo** simply [download this file](/md-templates/article/index.md) (or copy the contents displayed, depending on your browser) and work on it using your favourite text editor.

## 2b. Front matter

In the front matter for an article, the following fields are compulsory:

- `title`
- `subtitle`
- `authors` is an array that should look like `["Jane Doe","Betelguese","John Smith"]` (see the *Updating your author page* below for more)
- `syndication_link` should be a link to a webpage on your own website (if this article was originally published there)
- `date` should take the format `yyyy-mm-ddThh:mm:ss±hh:mm` (the last `±hh:mm` is your timezone but leave it as `+00:00` if in doubt)
- `type` should be `article`
- `draft` should be remain `true`

The file you created using Hugo, or downloaded above if you went that route, will have other front matter fields like `cover` and `tags` (see FAQs below for more).

Type the main content of your article after the `---` at the end of the front matter. There is no word limit.

## 2c. Submitting your article

If you used Git and Hugo, simply submit a pull request to submit your article.

If you downloaded the file above, simply e-mail the file to [James G](mailto:readers@jamesg.blog) or [V.H. Belvadi](mailto:hello@vhbelvadi.com) and we will line it up for publication.

All articles submitted will be published together as part of an upcoming issue of *Anthologies*. Articles will not be published independently or immediately upon submission. To help with this, please ensure your `draft` status is set to `true`.

***

# 3. Updating your author page

Everyone who has made at least one contribution to WWC – whether that is an article in *Anthologies* or a notice posted on our noticeboard – *will* have an author page that is created automatically. It is therefore *extremely* important that you—

* ensure that the first time you save your author name in the `authors` field in the front matter (see above) your name is saved as you would like it to be saved
* ensure you use the author slug as Hugo (and therefore this website) programmatically generates it to be (using a slug of your choice can break the link)

[Here are](/authors/v.h.-belvadi) [examples of](/authors/james-g) author pages. *All of this section is optional.* When you publish something on WWC you will already have an author page. This sections exists simply to give you the opportunity to add a few lines to your author page and make it more approachable or, more importantly, to help someone who stumbles upon your articles or notices on WWC also find their way to your website.

Before starting, [visit your author page](/authors/) and note down the URL. Note particularly, the hyphens and full stops. If your name is `J.D. Salinger` and you put in, say, `authors: ["Emily Brontë","J.D. Salinger"]` in your notice or article published on this website, you will find that your author page URL ends with `/authors/j.d.-salinger` and not `/authors/jd-salinger` or some other variant. 

This is important for two reasons: firstly, this means your `title` (more on this below) in your author page must also be `J.D. Salinger` and not a variation; and secondly, any change to the `title`, `authors` or slug will break your author page links (everyone else’s will be safe). If you change one of these, you will have to change them all. If multiple variations are credited across multiple notices or articles, WWC will have no chocie but to treat you as multiple authors.

## 3a. Create your author page

**If you are familiar with Hugo** clone [this website’s repo](git@github.com:vhbelvadi/webwriterscollective.com.git), install Hugo and any dependencies if you have not done so already, and create your author page by running the following command from the terminal:

```
hugo new authors/firstname-lastname --kind author
```

This should give you file inside `content/authors/firstname-lastname` with the approproate front matter.

**If you are unfamiliar with Hugo** simply [download this file](/md-templates/author/_index.md) (or copy the contents displayed, depending on your browser) and work on it using your favourite text editor.

## 3b. Front matter

In the front matter for your author page, the following fields exist:

- `title` (despite what it looks like, this is your name and not your title – trust us – and should be *exactly* as it appears inside notes etc.)
- `name` (this is a short form of your name used e.g. to link to your website and possibly elsewhere in future; should you decide to leave it empty, we will use your `title` instead)
- `bio` is… your bio, *without HTML or markdown support* – just plain text
- `website` is a full link to your site, e.g. `https://indieweb.org`

Strictly speaking, the `bio`, `name` and `website` fields are optional. (Although, surely, you would want to link back to your website!) While your author page will function without doing anything in this section, once you *do* create this page, your author page will be associated with it permanently. That means leaving the `title` field blank will also show a blank name on the WWC website, so please fill it in.

Do not type anything else in this file. Typing in what is traditionally the ‘content’ area below the last `---` will do nothing. Please see the FAQ for troubleshooting author pages.

## 3c. Publishing your author page

If you used Git and Hugo, simply submit a pull request to publish your author page. Frequent contributors may request to be added to the repo to bypass this step (we are a community after all).

If you downloaded the file above, simply e-mail the file to [James G](mailto:readers@jamesg.blog) or [V.H. Belvadi](mailto:hello@vhbelvadi.com) and we will publish it for you. However, we cannot promise to publish it within tight deadlines.

***

# FAQs

## I don’t know markdown

*That’s OK!* You can convert rich text to markdown in many ways. If you would like to learn markdown (and we certainly recommend it) there are plenty of [wonderful websites](https://learnxinyminutes.com/markdown/) on which to get started. If you use an Apple device, for example, you can type rich text in your Notes app (as of OS 27) and *copy as markdown*. Android and Windows devices offer similar features, or you can use a [web-based docx convertor](https://word2md.com/). All said and done, we still think it is simpler, not to mention quick and easy, to learn markdown.

## How do I add images?

Simply place the image file next to your `index.md` file and refer to it by name and extension. *Please do not place image files anywhere else.* Using images as cover is the same; specify the image in the frontmatter against the `cover` field.

## I got the issue number wrong…

If you typed the issue number wrong while creating a new article within Hugo, we have fallbacks in place to ensure your article does not get lost. It will, however, be misplaced because it has been filed under the wrong issue. Just [let us know](mailto:readers@jamesg.blog) and we will fix it for you.

## My author page has a problem

If your author page (a) is not showing up or (b) is missing articles and/or notices please check the following. First, ensure that your name across all your submissions is identical. Second, ensure that name matches exactly what you have filled in against `title` in the front matter of your author page. Third, 

## What is the `tags` field?

You might notice the `tags` field in the front matter of notices and articles, but no tags anywhere on this website. We do not currently use tags in order to prevent cluttering up this website, but we like to keep writings tagged for when we think of a more creative but unclutterred use in the future. The `tags` field works like the `authors` field, i.e. as an array (see above for more on the `authors` field). We do not prescribe *how* you should tag something, but we request that you tag sensibly so as not to end up with multiple competing variations of the same tag across the site, e.g. travel, travelling, traveling, travels.

## I have a question not answered here (or an idea)

Please [get in touch](mailto:hello@vhbelvadi.com) and we will help you (or appreciate your idea).
