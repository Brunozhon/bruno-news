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
    <td align="left"><img src="https://github.com/Brunozhon/bruno-news/assets/69879040/b6257199-d159-447e-8c2f-63a20ed6ca5a" height="245" width="175"/></td>
    <td align="left" valign="bottom" class="text-start"><p>
<span style="font-size: 30px;"><b>Zichun Zhong</b></span>
<br/><br/>
<b>Associate Professor</b><br/>
<a href="https://engineering.wayne.edu/cs/">Department of Computer Science</a><br/>
<a href="https://wayne.edu/">Wayne State University</a><br/>
<br/>
<b>Tel: </b>REDACTED (office)<br/>
<b>Fax: </b>REDACTED<br/>
<b>Email:</b>REDACTED<br/> <br/>
<b>Office: </b>REDACTED<br/>
<b>Computer Modeling and Imaging Visualization Lab: </b>REDACTED<br/>
<b>Graphics and Imaging Lab: </b>REDACTED<br/>
</p></td>
  </tr>
</table>

And here's the code of the table after some editing to conform to HTML5:

```html
<table>
  <tr>
    <td align="left"><img src="https://github.com/Brunozhon/bruno-news/assets/69879040/b6257199-d159-447e-8c2f-63a20ed6ca5a" height="245" width="175"/></td>
    <td align="left" valign="bottom"><p>
<span style="font-size: 30px;"><b>Zichun Zhong</b></span>
<br/><br/>
<b>Associate Professor</b><br/>
<a href="https://engineering.wayne.edu/cs/">Department of Computer Science</a><br/>
<a href="https://wayne.edu/">Wayne State University</a><br/>
<br/>
<b>Tel: </b>REDACTED (office)<br/>
<b>Fax: </b>REDACTED<br/>
<b>Email:</b>REDACTED<br/> <br/>
<b>Office: </b>REDACTED<br/>
<b>Computer Modeling and Imaging Visualization Lab: </b>REDACTED<br/>
<b>Graphics and Imaging Lab: </b>REDACTED<br/>
</p></td>
  </tr>
</table>
```

Using Bootstrap's grid system, we can get this:

<div class="container text-center">
  <div class="row">
    <div class="col-auto">
      <img src="https://github.com/Brunozhon/bruno-news/assets/69879040/b6257199-d159-447e-8c2f-63a20ed6ca5a" height="245" width="175"/>
    </div>
    <div class="col">
      <p><span style="font-size: 30px;"><b>Zichun Zhong</b></span></p>
      <p>
        <b>Associate Professor</b><br/>
        <a href="https://engineering.wayne.edu/cs/">Department of Computer Science</a><br/>
        <a href="https://wayne.edu/">Wayne State University</a><br/>
      </p>
      <p>
        <b>Tel: </b>REDACTED (office)<br/>
        <b>Fax: </b>REDACTED<br/>
        <b>Email:</b> REDACTED
      </p>
      <p>
        <b>Office: </b>REDACTED<br/>
        <b>Computer Modeling and Imaging Visualization Lab: </b>REDACTED<br/>
        <b>Graphics and Imaging Lab: </b>REDACTED
      </p>
    </div>
  </div>
</div>

And here's the code:

```html
<div class="container text-center">
  <div class="row">
    <div class="col-4">
      <img src="https://github.com/Brunozhon/bruno-news/assets/69879040/b6257199-d159-447e-8c2f-63a20ed6ca5a" height="245" width="175"/>
    </div>
    <div class="col-8">
      <p><span style="font-size: 30px;"><b>Zichun Zhong</b></span></p>
      <p>
        <b style="font-size: 4.5px;">Associate Professor</b><br/>
        <a href="https://engineering.wayne.edu/cs/">Department of Computer Science</a><br/>
        <a href="https://wayne.edu/">Wayne State University</a><br/>
      </p>
      <p>
        <b>Tel: </b>REDACTED (office)<br/>
        <b>Fax: </b>REDACTED<br/>
        <b>Email:</b> REDACTED
      </p>
      <p>
        <b>Office: </b>REDACTED<br/>
        <b>Computer Modeling and Imaging Visualization Lab: </b>REDACTED<br/>
        <b>Graphics and Imaging Lab: </b>REDACTED
      </p>
    </div>
  </div>
</div>
```
