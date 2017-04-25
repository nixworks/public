
## API

*the Context* aims to be an Open Website. Therefore, access to this website and its API is free, open, unmonitored, unlimited, possible in different formats and licensed under a permissive [CC BY-SA 3.0](https://en.wikipedia.org/wiki/Wikipedia:Text_of_Creative_Commons_Attribution-ShareAlike_3.0_Unported_License) license.

*the Context* news content is based on Wikipedia Current Events Portal and the API is very simple: each HTML page is also available in Markdown, JSON or XML. It's enough to change `.html` in the URL into an appropriate extension: `.md`, `.json` or `.xml`. Therefore, to access latest news on the front page and read them using JSON, it's enough to query [thecontext.net/index.json](http://thecontext.net/index.json). If encryption is necessary, all URLs are also available via HTTPS.

Each page is versioned using GitHub, and its history is available by substituting the URLs the domain `http://thecontext.net` to `https://github.com/thecontextnet/public/commits/master`. For example, the history of the front page is available at [github.com/thecontextnet/public/commits/master/index.html](https://github.com/thecontextnet/public/commits/master/index.html). Of course, history is available for different file formats, therefore it's possible to access that file for example in Markdown: [github.com/thecontextnet/public/commits/master/index.md](https://github.com/thecontextnet/public/commits/master/index.md).

### API Tree

Exact website file tree is visible on [*the Context* webstie source code](https://github.com/thecontextnet/public) repository on GitHub. However, the most important information is structured as follows:

- /index, (html, xml, json, md), the front page, list with news files from the last 3 days
  - /news, contains the information from Wikipedia Current Events Portal
    - /news/[YYYY], 4-digit year
      - /news/[YYYY]/[MM], 2-digit month with leading zero
        - /news/[YYYY]/[MM]/[DD], 2-digit day without leading zero
          - /news/[YYYY]/[MM]/[DD]/index, (html, xml, json, md), list with all available news files for this day
          - /news/[YYYY]/[MM]/[DD]/[title], (html, xml, json, md), the content of a single news, source metadata, related items
  - /opinion, contains dedicated editorial content
    - /opinion/index, (html, xml, json, md), list with all available opinion editorials
    - /opinion/[YYYY], 4-digit year
      - /opinion/[YYYY]/[MM], 2-digit month with leading zero
        - /opinion/[YYYY]/[MM]/[DD], 2-digit day without leading zero
          - /opinion/[YYYY]/[MM]/[DD]/index, (html, xml, json, md), the content of a single editorial

### Source code and data

Each of the repositories below is updated every 2 hours, with timestamps according to UTC.

* [*the Context* website source code](https://github.com/thecontextnet/public) - contains the same data as available at [thecontext.net](http://thecontext.net), but limited to last 2 years because of the 1GB repository size limit on GitHub
* [Raw source of the English Wikipedia Current Events Portal](https://github.com/thecontextnet/wiki-raw) - contains the data from 1999 until today in wiki syntax
* [Open Graph metadata of URLs marked as news source](https://github.com/thecontextnet/wiki-meta) - contains each news source metadata stored in a hash-named file, corresponding to the news source hash available through *the Context* API

### RSS Feeds

Additionally, two RSS feeds in XML format are available:

- News Feed at [thecontext.net/index_rss.xml](http://thecontext.net/index_rss.xml)
- Opinions Feed at [thecontext.net/opinion_rss.xml](http://thecontext.net/opinion_rss.xml)

### Bugs and Issues

The best place to report bugs and issues is via the [GitHub Issues of the Public repository](https://github.com/thecontextnet/public/issues).

*the Context* can be contacted via email at [editor@thecontext.net](mailto:editor@thecontext.net)