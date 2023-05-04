---
title: What is robots.txt
author: mohit
type: post
date: 2020-11-06T03:15:23+00:00
draft: true
url: /?p=71
neve_meta_enable_content_width:
  - off
  - off
categories:
  - Web

---
The robots.txt file is a text file that defines which parts of a domain can be crawled by a Webcrawler, and which parts can&#8217;t be. In addition, the robots.txt file can include a link to the XML-sitemap. With robots.txt, individual files in a directory, complete directories, subdirectories or entire domains can be excluded from crawling. The robots-txt data is stored in the root of the domain. It is the first document that is accessed by a bot when it visits a website. The bots of the biggest search engines such as Google and Bing follow the instructions. Otherwise there is no guarantee that a bot will adhere to the robots.txt requirements.

Robots.txt is stored in the root directory of a domain. Thus it is the first document that crawlers open when visiting your site. However, the file does not only control crawling. You can also integrate a link to your sitemap, which gives search engine crawlers an overview of all existing URLs of your domain.

&nbsp;

## <span id="How_robots.txt_works" class="mw-headline">How robots.txt works</span>

In 1994, a protocol called REP (Robots Exclusion Standard Protocol) was published. This protocol stipulates that all search engine crawlers (user-agents) must first search for the robots.txt file in the root directory of your site and read the instructions it contains. Only then, robots can start indexing your web page. The file must be located directly in the root directory of your domain and must be written in lower case because robots read the robots.txt file and its instructions case-sensitive. Unfortunately, not all search engine robots follow these rules. At least the file works with the most important search engines like Bing, Yahoo, and Google. Their search robots strictly follow the REP and robots.txt instructions.

In practice, robots.txt can be used for different types of files. If you use it for image files, it prevents these files from appearing in the Google search results. Unimportant resource files, such as script, style, and image files, can also be blocked easily with robots.txt. In addition, you can exclude dynamically generated web pages from crawling using appropriate commands. For example, result pages of an internal search function, pages with session IDs or user actions such as shopping carts can be blocked. You can also control crawler access to other non-image files (web pages) by using the text file. Thereby, you can avoid the following scenarios:

  * search robots crawl lots of similar or unimportant web pages
  * your crawl budget is wasted unnecessarily
  * your server is overloaded by crawlers

In this context, however, note that robots.txt does not guarantee that your site or individual sub-pages are not indexed. It only controls the crawling of your website, but not the indexation. If web pages are not to be indexed by search engines, you have to set the following meta tag in the header of your web page:

<pre>&lt;meta name="robots" content="noindex"&gt;</pre>

However, you should not block files that are of high relevance for search robots. Note that CSS and JavaScript files should also be unblocked, as these are used for crawling especially by mobile robots.

## <span id="Which_instructions_are_used_in_robots.txt.3F" class="mw-headline">Which instructions are used in robots.txt?</span>

Your robots.txt has to be saved as a UTF-8 or ASCII text file in the root directory of your web page. There must be only one file with this name. It contains one or more rule sets structured in a clearly readable format. The rules (instructions) are processed from top to bottom whereby upper and lower case letters are distinguished.

The following terms are used in a robots.txt file:

  * user-agent: denotes the name of the crawler (the names can be found in the Robots Database)
  * disallow: prevents crawling of certain files, directories or web pages
  * allow: overwrites disallow and allows crawling of files, web pages, and directories
  * sitemap (optional): shows the location of the sitemap
  * *: stands for any number of character
  * $: stands for the end of the line

The instructions (entries) in robots.txt always consist of two parts. In the first part, you define which robots (user-agents) the following instruction apply for. The second part contains the instruction (disallow or allow). &#8220;user-agent: Google-Bot&#8221; and the instruction &#8220;disallow: /clients/&#8221; mean that Google bot is not allowed to search the directory /clients/. If the entire website is not to be crawled by a search bot, the entry is: &#8220;user-agent: _&#8221; with the instruction &#8220;disallow: /&#8221;. You can use the dollar sign &#8220;$&#8221; to block web pages that have a certain extension. The statement &#8220;disallow: /_ .doc$&#8221; blocks all URLs with a .doc extension. In the same way, you can block specific file formats n robots.txt: &#8220;disallow: /*.jpg$&#8221;.

For example, the robots.txt file for the website https://www.example.com/ could look like this:

<pre>User-agent: *
Disallow: /login/
Disallow: /card/
Disallow: /fotos/
Disallow: /temp/
Disallow: /search/
Disallow: /*.pdf$

Sitemap: https://www.example.com/sitemap.xml</pre>

## <span id="What_role_does_robots.txt_play_in_search_engine_optimization.3F" class="mw-headline">What role does robots.txt play in search engine optimization?</span>

The instructions in a robots.txt file have a strong influence on SEO (Search Engine Optimization) as the file allows you to control search robots. However, if user agents are restricted too much by disallow instructions, this has a negative effect on the ranking of your website. You also have to consider that you won’t rank with web pages you have excluded by disallow in robots.txt. If, on the other hand, there are no or hardly any disallow restrictions, it can happen that pages with duplicate content are indexed, which also has a negative effect on the ranking of these pages.

Before you save the file in the root directory of your website, you should check the syntax. Even minor errors can lead to search bots disregarding the disallow rules and crawling websites that should not be indexed. Such errors can also result in pages no longer being accessible for search bots and entire URLs not being indexed because of disallow. You can check the correctness of your robots.txt using Google Search Console. Under &#8220;Current Status&#8221; and &#8220;Crawl Errors&#8221;, you will find all pages blocked by the disallow instructions.

By using robots.txt correctly you can ensure that all important parts of your website are crawled by search bots. Consequently, your entire page content is indexed by Google and other search engines.

## <span id="Related_links" class="mw-headline">Related links</span>

  * <a class="external free" href="https://support.google.com/webmasters/answer/6062608?hl=en" rel="nofollow">https://support.google.com/webmasters/answer/6062608?hl=en</a>
  * <a class="external free" href="https://support.google.com/webmasters/answer/6062596?hl=en" rel="nofollow">https://support.google.com/webmasters/answer/6062596?hl=en</a>