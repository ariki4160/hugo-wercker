+++
date = "2016-05-02T23:25:36+09:00"
draft = false
title = "Post title"
slug = "post-title"
tags = ["tag1","tag2"]
image = "/images/20160502/ariki.jpg"
comments = true	# set false to hide Disqus
share = true	# set false to hide share buttons
menu= "main"		# set "main" to add this content to the main menu
author = "Masayuki Ariki"


+++

## Multiple authors configuration

In addition to providing data for a single author as shown in the example above, multiple authors can be configured via data/authors/*.(yml, toml, json) entries. If the key provided in .Site.Params.author matched a data/authors/* entry, it will be used as the default. Overrides per page can be done by a simple author = other_author_key entry in the front matter. For those pages where you want to omit the author block completely, a .Params.noauthor entry is also available.