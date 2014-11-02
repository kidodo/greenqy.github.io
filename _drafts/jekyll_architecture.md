---
layout: default
---

jekyll 结构
============

目录结构
-------
jekyll 目录结构如下：
    .
    ├── _config.yml
    ├── _drafts
    |   ├── begin-with-the-crazy-ideas.textile
    |   └── on-simplicity-in-technology.markdown
    ├── _includes
    |   ├── footer.html
    |   └── header.html
    ├── _layouts
    |   ├── default.html
    |   └── post.html
    ├── _posts
    |   ├── 2007-10-29-why-every-programmer-should-play-nethack.textile
    |   └── 2009-04-26-barcamp-boston-4-roundup.textile
    ├── _data
    |   └── members.yml
    ├── _site
    └── index.html


配置文件 _config.yml
--------------------
### 配置文件的默认值：
文档[地址](http://jekyllrb.com/docs/configuration/)

    # Where things are
    source:      .
    destination: ./_site
    plugins:     ./_plugins
    layouts:     ./_layouts
    data_source: ./_data
    collections: null
    
    # Handling Reading
    safe:         false
    include:      [".htaccess"]
    exclude:      []
    keep_files:   [".git", ".svn"]
    encoding:     "utf-8"
    markdown_ext: "markdown,mkdown,mkdn,mkd,md"
    textile_ext:  "textile"
    
    # Filtering Content
    show_drafts: null
    limit_posts: 0
    future:      true
    unpublished: false
    
    # Plugins
    whitelist: []
    gems:      []
    
    # Conversion
    markdown:    kramdown
    highlighter: pygments
    lsi:         false
    excerpt_separator: "\n\n"
    
    # Serving
    detach:  false
    port:    4000
    host:    0.0.0.0
    baseurl: "" # does not include hostname
    
    # Backwards-compatibility
    relative_permalinks: false
    
    # Outputting
    permalink:     date
    paginate_path: /page:num
    timezone:      null
    
    quiet:    false
    defaults: []
    
    # Markdown Processors
    maruku:
      use_tex:    false
      use_divs:   false
      png_engine: blahtex
      png_dir:    images/latex
      png_url:    /images/latex
      fenced_code_blocks: true
    
    rdiscount:
      extensions: []
    
    redcarpet:
      extensions: []
    
    kramdown:
      auto_ids:      true
      footnote_nr:   1
      entity_output: as_char
      toc_levels:    1..6
      smart_quotes:  lsquo,rsquo,ldquo,rdquo
      use_coderay:   false
    
      coderay:
        coderay_wrap:              div
        coderay_line_numbers:      inline
        coderay_line_number_start: 1
        coderay_tab_width:         4
        coderay_bold_every:        10
        coderay_css:               style
    
    redcloth:
      hard_breaks: true

参考
----
[Official Documents](http://jekyllrb.com/docs/home/)
