所有主题都包含style.css文件，它控制着主题呈现出来的样子（视觉设计和布局）。

## 位置

为了确保有效地组织这些模板文件成为一个有效的主题，style.css文件必须放在主题根目录，而不是二级目录。

## 文件基本结构

WordPress会使用style.css头部注释代码段的一些信息，在后台>外观>主题中显示。

## 举例

```
/*
Theme Name: Twenty Seventeen
Theme URI: https://wordpress.org/themes/twentyseventeen/
Author: the WordPress team
Author URI: https://wordpress.org/
Description: Twenty Seventeen brings your site to life with immersive featured images and subtle animations. With a focus on business sites, it features multiple sections on the front page as well as widgets, navigation and social menus, a logo, and more. Personalize its asymmetrical grid with a custom color scheme and showcase your multimedia content with post formats. Our default theme for 2017 works great in many languages, for any abilities, and on any device.
Version: 1.0
License: GNU General Public License v2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Text Domain: twentyseventeen
Tags: one-column, two-columns, right-sidebar, flexible-header, accessibility-ready, custom-colors, custom-header, custom-menu, custom-logo, editor-style, featured-images, footer-widgets, post-formats, rtl-language-support, sticky-post, theme-options, threaded-comments, translation-ready
This theme, like WordPress, is licensed under the GPL.
Use it to make something cool, have fun, and share what you've learned with others.
*/
```

说明：

- Theme Name (*)： 主题名字。
- Theme URI：可访问的公开的可以让用户了解更多主题信息的网址。
- Author (*)：开发主题的个人或者组织名称，当然还是推荐使用你在wordpress.org的用户名。
- Author URI：主题作者个人或者组织的网址。
- Description (*)：主题的介绍。
- Version (*)：版本号, 建议写成 X.X 或者 X.X.X 的格式。
- License (*)：主题的版本声明，当然这只能是“GNU General Public License v2 or later”，不要改为其他的。
- License URI (*)：版权声明的网址。
- Text Domain (*)：为翻译准备的“域”字段，比如我开发的主题通常是 lean。
- Tags: 允许用户使用的可以在wordpress主题目录筛选的一些文字或者短语. 回头我会为大家找到所有可以使用的标签。


现在比如我们要创建名称为：myTheme的主题：
1. 创建目录myTheme；
2. 在根目录创建一个style.css，将上面代码贴进去修改成你的主题名字；
3. 上传文件夹到wp-content/themes；

即可在后台》外观》主题那里看到自己的主题。