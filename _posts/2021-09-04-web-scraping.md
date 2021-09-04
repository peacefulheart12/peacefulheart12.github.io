---
title: "Web Scraping in R"
summary: "Scraping movie Data from IMDB with the rvest package"
layout: post
author: Gaurav Tiwari
thumbnail: Downloads/webapp
---
I used to think web scraping sounded complicated. You’d have to decode a bunch of HTML and Javascript and do messy hacking to get at what you wanted.
But once I took a crack at it using my favourite language of R, I realized that tools exist to make it very tidy and straightforward, and I was surprised by how quickly and easily I was pulling facts, tables, images and various other assets from websites.
So I’ve written up a step by step guide to get you started. You can also find the Markdown version of this guide and the various functions and assets I created here so you can execute them in your R session.
Hope you find this helpful!
1. Web Page Structure and Format
Any webpage you visit has a particular, expected general structure. It usually consists of two types of code.
HTML code, which focuses on the appearance and format of a web page.
XML code, which doesn’t look a lot different from HTML but focuses more on managing data in a web page.
1.1 HTML code
HTML code has an expected format and structure, to make it easy for people to develop web pages. Here is an example of a simple HTML page:
<img src="Downloads/webapp.png" alt="Web">
As you can see, the content is wrapped in tags like <head>, <body>, <p>. These tags are pre-defined by the language (you can only use the tags that HTML allows). Because HTML has a more predictable structure, it is often easier to work with it and mine it.
1.2 XML code
XML format and structure is less predictable. Although it looks very similar to HTML, users can create their own named tags. Here is an example:
Tags like <to> and <from> are completely made up by me. The fact that tags are not pre-defined makes XML a little harder to mine and analyze. But it’s hard to get at some of the data on the web without using XML.
