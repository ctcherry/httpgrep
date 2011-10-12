httpgrep
========

Helps to filter and work with the response codes given by URLs.

Examples
--------

Annotation - add the response code to the output with the URL

```bash
$ echo -e "http://google.com\nhttp://www.reddit.com" | ruby httpgrep -a
301; http://google.com
200; http://www.reddit.com
```

Exclude provided response codes from output

```bash
$ echo -e "http://google.com\nhttp://www.reddit.com" | ruby httpgrep --exclude 301
http://www.reddit.com
```