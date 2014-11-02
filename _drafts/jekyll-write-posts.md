---
layout: default
---

jekyll posts
============

文件名
-----
    YEAR-MONTH-DAY-title.MARKUP

分类/标签
--------



插入图片/资源
-------------

在根目录下建立一个文件夹 `assets`

    ![My helpful screenshot]({{ site.url }}/assets/screenshot.jpg)
    [get the PDF]({{ site.url }}/assets/mydoc.pdf)


文章摘要
--------
默认把post中的第一块文字到 `excerpt_seperator` 之间的内容作为摘要 `post.excerpt`。

显示文章索引
-----------
    <ul>
        {% for post in site.posts %}
            <li>
                <a href=“{{ post.url}}”>{{ post.title }}</a>
                {{ post.excerpt }}
            </li>
        {% endfor %}
    </ul>

高亮显示code
------------
在 _config.yml 中设置 `highlighter` 为 `pygments` 或者 `rouge`, 指定使用哪一个来转化高亮。

* [pygments]() 支持100多种语言，但是需要后台安装python。
* [rouge]() 支持的语言要少一点，但是因为本身是ruby写的，所以没有额外的依赖, [支持的语言](rouge support list)。

 [pygments](http://pygments.org/)
 [rouge](https://github.com/jayferd/rouge)
 [rouge support list](http://rouge.jayferd.us/demo)


高亮显示为 ruby, 并包含行号：
    {% highlight ruby linenos %}
    def show
      @widget = Widget(params[:id])
      respond_to do |format|
        format.html # show.html.erb
        format.json { render json: @widget }
      end
    end
    {% endhighlight %}

