# 内容类型（ Post Types ）

** 这一节对理解模板等级非常重要。**

在 wordpress 中有很多不同的内容类型。这些内容类型被称为 Post Types，你可能或许有些混乱，因为它关联wordpress中所有不同的内容类型。例如：“文章”，是一种特殊的内容类型，也是一个“页面”。

本质上，所有的内容类型都会被存储在数据库 wp_posts 这个表中，但是在数据库中通过 post_type 区分。

如果你想增加默认的内容类型，你可以创建一个内容类型。

模板文件页面显示的是根据不同模板文件来显示不同的内容类型，由于模板文件目的是以某种形式显示内容，所以实际上内容类型就是为了给你正在处理的内容进行一种分类。简单来说，某些内容类型与某些模板文件是绑定在一起的。

## 默认的内容类型

wordpress在安装时，有五种默认的内容类型：

- 文章 (Post Type: ‘post’)
- 页面 (Post Type: ‘page’)
- 多媒体 (Post Type: ‘attachment’)
- 版本 (Post Type: ‘revision’)
- 菜单 (Post Type: ‘nav_menu_item’)

这些内容类型都是通过主题或者插件定制或者移除，但是我们不建议在主题和插件中删除内置功能。

The most common post types you will interact with as a Theme Developer are Post, Page, Attachment, and Custom Post Types.  It’s out of the scope of this handbook to flesh out the Revision and Navigation Menu Post Types.  However, it is important to note that you will interact with and build the functionality of navigation menus and that will be detailed later in this handbook.

## 文章（ Post ）

Posts are used in blogs. They are:

- displayed in reverse sequential order by time, with the newest post first
- have a date and time stamp
- may have the default taxonomies of categories and tags applied
- are used for creating feeds

The template files that display the Post post type are:

- single.php and single-post.php
- category.php and all its iterations
- tag.php and all its iterations
- taxonomy.php and all its iterations
- archive.php and all its iterations
- author.php and all its iterations
- date.php and all its iterations
- search.php
- home.php
- index.php

Additionally, theme developers can display Post post types in front-page.php if they so desire.

## 页面（ Page ）

Pages are a static Post Type, outside of the normal blog stream/feed. Their features are:

- non-time dependent and without a time stamp
- are not organized using the categories and/or tags taxonomies
- can have page templates applied to them
- can be organized in a hierarchical structure — i.e. pages can be parents/children of other pages

The template files that display the Page post type are:

- page.php and all its iterations
- $custom.php and all its iterations
- front-page.php
- search.php
- index.php


## 多媒体（ Attachment ）

Attachments are commonly used to display images or media in content, and may also be used to link to relevant files. Their features are:

- contain information (such as name or description) about files uploaded through the media upload system
- for images, this includes metadata information stored in the wp_postmeta table (including size, thumbnails, location, etc)

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
