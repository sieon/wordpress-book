# 内容类型（ Post Types ）

** 这一节对理解模板等级非常重要。**

在 WordPress 中有很多不同的内容类型。这些内容类型被称为 Post Types，你可能或许有些混乱，因为它关联WordPress中所有不同的内容类型。例如：“文章”，是一种特殊的内容类型，也是一个“页面”。

本质上，所有的内容类型都会被存储在数据库 wp_posts 这个表中，但是在数据库中通过 post_type 区分。

如果你想增加默认的内容类型，你可以创建一个内容类型。

模板文件页面显示的是根据不同模板文件来显示不同的内容类型，由于模板文件目的是以某种形式显示内容，所以实际上内容类型就是为了给你正在处理的内容进行一种分类。简单来说，某些内容类型与某些模板文件是绑定在一起的。

## 默认的内容类型

WordPress在安装时，有五种默认的内容类型：

- 文章 (内容类型: ‘post’)
- 页面 (内容类型e: ‘page’)
- 多媒体 (内容类型: ‘attachment’)
- 版本 (内容类型: ‘revision’)
- 菜单 (内容类型: ‘nav_menu_item’)

这些内容类型都是通过主题或者插件定制或者移除，但是我们不建议在主题和插件中删除内置功能。

一个主题开发者最长接触到的是 文章、页面、附件和自定义内容类型。版本与菜单内容类型不在我们这本手册的范围内，不过，重要的是要注意，导航菜单的功能也是经常会用到的，在本手册后面详细介绍这些功能。

## 文章（ Post ）

文章类型常用于博客，如下：

- 按时间倒叙显示，首先显示最新的文章；
- 有日期和时间标记；
- 可能应用默认类别和标签；
- 用于创建 feeds；

显示文章类型的模板文件如下：

- single.php 和 single-post.php
- category.php
- tag.php
- taxonomy.php
- archive.php
- author.php
- date.php
- search.php
- home.php
- index.php

此外，主题开发者按照意愿可以在front-page.php显示文章。

## 页面（ Page ）

页面是一种静态的内容类型，通常不在博客内容流和feed中显示，它们的特色：

- 不依赖时间戳
- 不用分类目录和标签这种分类组织
- 可以拥有自己的模板文件
- 可以有父子等级结构

显示页面的模板文件如下：

- page.php
- $custom.php
- front-page.php
- search.php
- index.php


## 附件（ Attachment ）

附件通常用于在内容中显示图片和多媒体，或许用于链接到相关的文件。它们的特点：

- contain information (such as name or description) about files uploaded through the media upload system
- for images, this includes metadata information stored in the wp_postmeta table (including size, thumbnails, location, etc)
- 


The template files that display the Attachment post type are:

- MIME_type.php
- attachment.php
- single-attachment.php
- single.php
- index.php

## 自定义内容类型（ Custom Post Types ）

Using Custom Post Types, you can create your own post type. It is not recommend that you place this functionality in your theme. This type of functionality should be placed/created in a plugin. This ensures the portability of your user’s content, and that if the theme is changed the content stored in the Custom Post Types won’t disappear.

You can learn more about creating custom post types in the WordPress Plugin Developer Handbook.

While you generally won’t develop Custom Post Types in your theme, you may want to code ways to display Custom Post Types that were created by a plugin.  The following templates can display Custom post types:

- single-{post-type}.php
- archive-{post-type}.php
- search.php
- index.php

Additionally, Theme Developers can display Custom Post Types in any template file, often by using multiple loops.
