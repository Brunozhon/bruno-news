---
layout: post
title: Improving Dad's Homepage - Making it Conform to Modern Standards (Part 1)
author: Bruno Zhong
excerpt_separator: <!-- more -->
---

Have you ever thought a website was too old? No problem, because today I'll be improving dad's website.

This is a multi-part project. In this part I will focus on making Dad's homepage's HTML conform to modern guidelines. Here are all the other parts:

<!-- more -->

1. Improving Dad's Homepage - Making it Conform to Modern Standards

## Fixing the Tables

It turns out that Dad's website has a lot of tables that are used for layout. Tables should **NEVER** be used for layout. You can use [Bootstrap's grid system](https://getbootstrap.com/docs/5.3/layout/grid/) for much better results.

### Table 1: The Introduction to Himself

Here's what the table looks like:

<table>
  <tr>
    <td align="left" width="200"><div style="width: 175px; height: 245px;">Image Placeholder</div></td>
    <td align="left" valign="bottom"><p>
<span style="font-size: 30px;"><b>Zichun Zhong</b></span>
<br/><br/>
<b style="font-size: 4.5px;">Associate Professor</b><br/>
<a href="https://engineering.wayne.edu/cs/">Department of Computer Science</a><br/>
<a href="https://wayne.edu/">Wayne State University</a><br/>
<br/>
<b>Tel: </b>313-577-9530 (office)<br/>
<b>Fax: </b>313-577-6868<br/>
<b>Email:</b> zichunzhong "at" wayne.edu<br/> <br/>
<b>Office: </b>5057 Woodward Ave. (Maccabees Building), Suite 14109.2, Detroit, Michigan, 48202<br/>
<b>Computer Modeling and Imaging Visualization Lab: </b>5057 Woodward Ave. (Maccabees Building), 2209, Detroit, Michigan, 48202<br/>
<b>Graphics and Imaging Lab: </b>5057 Woodward Ave. (Maccabees Building), 3104.5, Detroit, Michigan, 48202<br/>
</p></td>
  </tr>
</table>

And here's the code of the table after some editing to conform to HTML5:

```html
<table>
  <tr>
    <td align="left" width="200"><div style="width: 175px; height: 245px;">Image Placeholder</div></td>
    <td align="left" valign="bottom"><p>
<span style="font-size: 30px;"><b>Zichun Zhong</b></span>
<br/><br/>
<b style="font-size: 4.5px;">Associate Professor</b><br/>
<a href="https://engineering.wayne.edu/cs/">Department of Computer Science</a><br/>
<a href="https://wayne.edu/">Wayne State University</a><br/>
<br/>
<b>Tel: </b>313-577-9530 (office)<br/>
<b>Fax: </b>313-577-6868<br/>
<b>Email:</b> zichunzhong "at" wayne.edu<br/> <br/>
<b>Office: </b>5057 Woodward Ave. (Maccabees Building), Suite 14109.2, Detroit, Michigan, 48202<br/>
<b>Computer Modeling and Imaging Visualization Lab: </b>5057 Woodward Ave. (Maccabees Building), 2209, Detroit, Michigan, 48202<br/>
<b>Graphics and Imaging Lab: </b>5057 Woodward Ave. (Maccabees Building), 3104.5, Detroit, Michigan, 48202<br/>
</p></td>
  </tr>
</table>
```
