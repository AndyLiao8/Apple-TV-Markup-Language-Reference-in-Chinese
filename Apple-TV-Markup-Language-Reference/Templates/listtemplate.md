####listTemplate
列表模板（*listTemplate*）用来显示列表数据；比如，把用收藏的电影列出来，无论你是使用*catalogTemplate*去显示产品信息（动作电影，喜剧和收藏的电影），你要使用*listTemplate* 去显示分类的的内容，例如用户的收藏电影列表，所有项都显示屏幕的右边，就象把它们归类成一块，当某一项被选中，选中块的信息就屏幕左边显示。图8-1展示了基本的listTemplate页面。

图8-1 

![lstTemplate](https://developer.apple.com/library/prerelease/tvos/documentation/LanguagesUtilities/Conceptual/ATV_Template_Guide/Art/ATV_temps_list_2x.png)

#####listTemplate模板主要的元素
列表8-1 TVML标记的主要元素，表8-1 对主要元素的描述

#####列表8-1

1. &lt;listTemplate&gt;
2. &lt;banner&gt;
3.  …
4.  &lt;/banner&gt;
5.  &lt;list&gt;
6.  &lt;header&gt;
7.  …
8.  &lt;/header&gt;
9.  &lt;section&gt;
10. &lt;listItemLockup&gt;
11. &lt;title&gt;…&lt;/title&gt;
12. &lt;relatedContent&gt;
13. …
14. &lt;/relatedContent&gt;
15. &lt;/listItemLockup
16. &lt;/section&gt;
17. &lt;/list&gt;
18. &lt;/listTemplate&gt;

#####图8-1

|    元素名称   |                   描述                    |
|-------------|------------------------------------------|
|banner       |包含背景信息和页面标题的元素。|
|header|描述这一块表示的内容|
|list|列listTemplate的内容|
|listItemLockup|包含涉及到一个列表项的所有信息，例如项目名称和图像，以及相关内容。|
|relatedContent|显示左边选中项的相关信息|
|section|把相关信息组织成一块，目的是为了更好的布局|

#####listTemplate例子

列表8-2 用TVML显示 listTemplate例子 图8-2，相关的效果图，在屏幕左边用图片各文本显示高亮项的相关内容。

列表8-2

	<document>
	<listTemplate>
	<list>
	<header>
	<title>Favorite Movies</title>
	</header>
         <section>
            <listItemLockup>
               <title>Movie 1</title>
               <relatedContent>
                  <lockup>
                     <img src="path to images on your server/Car_Movie_1920x1080.png" width="857" height="482" />
                     <title>Movie 1</title>
                     <description>A brief description for the first movie should go here.</description>
                  </lockup>
               </relatedContent>
            </listItemLockup>
            <listItemLockup>
               <title>Movie 2</title>
               <relatedContent>
                  <lockup>
                     <img src="path to images on your server/Car_Movie_800x600.png" width="857" height="482" />
                     <title>Movie 2</title>
                     <description>A brief description for the second movie should go here.</description>
                  </lockup>
               </relatedContent>
            </listItemLockup>
            <listItemLockup>
               <title>Movie 3</title>
               <relatedContent>
                  <lockup>
                     <img src="path to images on your server/Car_Movie_720x720.png" width="857" height="482" />
                     <title>Movie 3</title>
                     <description>A brief description for the third movie should go here.</description>
                  </lockup>
               </relatedContent>
            </listItemLockup>
         </section>
      </list>
      </listTemplate>
	</document>
	
图片8-2

![listTemplate](https://developer.apple.com/library/prerelease/tvos/documentation/LanguagesUtilities/Conceptual/ATV_Template_Guide/Art/listTemplateSS_2x.png)
        




