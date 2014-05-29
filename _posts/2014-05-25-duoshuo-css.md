---
author: stannis
date: 2014-5-25 10:20+08:00
layout: post
title: 自已修改适合本站风格的多说评论插件CSS
slug: duoshuo
categories:
- 网页研究
tags:
- duoshuo
- CSS
---
    
### 基于多说官方暗色线框主题修改，以下是全部CSS代码 ###

{% highlight css %}
/*duoshuo style */
#ds-thread #ds-reset .ds-powered-by {
display: none !important;
}
#ds-thread #ds-reset .ds-meta {
display: none !important;
}
#ds-thread #ds-reset .ds-comments {
margin: 0 0 !important;
}
#ds-thread #ds-reset .ds-replybox {
margin: 0 0 !important;
}
#ds-thread #ds-reset .ds-post-toolbar span {
display:none !important;
}

{% endhighlight %}
<!--more-->
{% highlight css %}

#ds-thread #ds-reset #ds-bubble {
background:rgba(26, 26, 26, 0.9) !important;
border:1px solid #444 !important;
}
#ds-thread #ds-reset #ds-bubble a:hover {
color:#aaa !important;
}
#ds-thread #ds-reset #ds-bubble a {
color:#777 !important;
}
#ds-thread #ds-reset .ds-arrow-down {
border-top: 5px solid #444 !important;
}
#ds-thread #ds-reset .ds-avatar {
background:none !important;
}
#ds-thread #ds-reset .ds-avatar img {
 -webkit-border-radius: 25px !important;
  -moz-border-radius: 25px !important;
  border-radius: 25px !important;
  -webkit-transition: -webkit-transform 0.4s ease-out;
  -moz-transition: -moz-transform 0.4s ease-out;
  transition: transform 0.4s ease-out;
}
#ds-thread #ds-reset .ds-avatar img:hover {
  -webkit-transform: rotateZ(360deg);
  -moz-transform: rotateZ(360deg);
  transform: rotateZ(360deg);
}
#ds-thread #ds-reset .ds-user-name {
color:#807B1B !important;
}
#ds-thread #ds-reset .ds-comment-body p {
color:#bbb !important;
}
#ds-thread #ds-reset .ds-login-buttons p {
color:#bbb !important;
}
#ds-thread #ds-reset .ds-highlight {
color: #088A29 !important;
}
#ds-thread #ds-reset .ds-sort a.ds-current, #ds-thread #ds-reset .ds-sort a:active {
border-bottom: 3px solid #075F1D !important;
}
#ds-thread #ds-reset .ds-sort a:hover {
border-bottom: 3px solid #088A29 !important;
}
#ds-thread #ds-reset li.ds-tab a.ds-current {
border-bottom: 3px solid #075F1D !important;
}
#ds-thread #ds-reset .ds-login-buttons .ds-more-services {
display:none !important;
}
#ds-thread #ds-reset .ds-time {
color:#777 !important;
}
#ds-thread #ds-reset .ds-comment-actions a {
color:#777 !important;
}
#ds-thread #ds-reset .ds-comment-actions a:hover {
color:#ccc !important;
}
#ds-thread #ds-reset .ds-textarea-wrapper {
margin-top:8px !important;
}
#ds-thread #ds-reset li.ds-post-placeholder {
color:#777 !important;
}

{% endhighlight %}