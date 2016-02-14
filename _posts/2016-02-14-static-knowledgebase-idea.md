---
layout: post
title: "Static Knowledgebase Idea"
category: Project Ideas
permalink: /static-knowledgebase-idea
---

I was recently thinking about developer-oriented knowledgebases and thought it would be a great idea to build a knowledgebase on a static blog engine like Jekyll or Hugo. Static blog engines have many desirable characteristics including ease of authorship. It seems like a static blog engine could be converted to a knowledgebase easily by changing the homepage navigation / layout and adding a search capability. I imagine a project like this could be very useful and would love to see it developed.

<!-- more -->

## Navigation

Unlike a blog which has articles listed by date, the top level navigation for the knowledgebase would be based on tag. Each tag would include it's most popular articles and think link to the tag page for more articles. Each tag could be in a div box. It may be worthwhile to have some override for tag ordering beyond alphabetical.

## Search

At this time [Algolia](https://www.algolia.com/) provides free search for up to 10,000 records and 100,000 operations per month. That's more than enough for sites to get started and popular sites can sign up for Algolia's paid plans.

## Authoring and Version Control

The power of of building a knowledgebase off of a static blog generator is, of course, to allow developers to author in markdown stored on GitHub or another version control system.

## Conclusion

Static blog generators are popular with developers due to their simplicity and integration with services like GitHub. By enhancing a static blog generator to behave like a knowledgebase, developers can provide the knowledgebase experience users are accustomed to while supporting the authoring environment they are accustomed to.

While I think this is a great idea, I don't have enough time to work on it now so if anyone is interested in this or knows of a project, please let me know :)
